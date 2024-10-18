# Monitoramento-Inteligente-com-o-Azure
az group create --name MeuGrupoDeRecursos --location eastus

az monitor log-analytics workspace create --resource-group MeuGrupoDeRecursos --workspace-name MeuWorkspace --sku "PerGB2018"
dotnet add package Microsoft.ApplicationInsights.AspNetCore
using Microsoft.ApplicationInsights.Extensibility;

public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddApplicationInsightsTelemetry("sua-chave-de-instrumentação");
    }
}
var telemetryClient = new TelemetryClient();
telemetryClient.TrackEvent("EventoPersonalizado", new Dictionary<string, string>
{
    { "Chave1", "Valor1" },
    { "Chave2", "Valor2" }
});
git remote add origin https://github.com/fernado889/Monitoramento-Inteligente-com-o-Azure.git
git branch -M main
git push -u origin main
