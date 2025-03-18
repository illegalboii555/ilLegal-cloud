      - name: Start Minecraft Server
        run: |
          mkdir -p minecraft
          cd minecraft
          wget -O server.jar https://papermc.io/api/v2/projects/paper/versions/1.20.1/builds/150/downloads/paper-1.20.1-150.jar
          echo "eula=true" > eula.txt
          nohup java -Xmx2G -Xms2G -jar server.jar nogui &
          sleep 600
