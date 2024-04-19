Bug repro:

    git clone https://github.com/strowk/nextjs-leak && cd nextjs-leak
    run yarn start & in bash
    save pid of yarn process server_pid=$!
    check processes running ps aux | grep next (there would be next start and next-server)
    run kill $server_pid to stop the server
    run ps aux | grep next to check what is still running
