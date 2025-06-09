FROM mcr.microsoft.com/mssql/server:2022-latest

USER root
# Create a new user
RUN useradd -m mssqluser

# Give permissions to MSSQL directories
RUN chown -R mssqluser /var/opt/mssql

# Switch to the new user
USER mssqluser

# Set environment variables
ENV ACCEPT_EULA=Y
ENV SA_PASSWORD=YourStrong@Passw0rd
ENV MSSQL_PID=Developer

# Expose MSSQL port
EXPOSE 1433

# Start SQL Server
CMD ["/opt/mssql/bin/sqlservr"]
