# Estudo de Caso: Análise de Comportamento de Web Crawlers em Interfaces de Chat e LLMs

## Visão Geral
Este estudo analisa o comportamento de indexação e pré-visualização de links (*Link Previews*) acionados por plataformas de grande escala ao processar URLs fornecidas em ambientes de conversação baseados em IA.

## Indicadores de Coleta (IOCs Observados)
* **User-Agent Identificado:** `meta-webindexer/1.1`
* **Infraestrutura de Origem:** Autonomous System da Meta, Inc. (`AS32934`)
* **Vetor de Acionamento:** Inserção de link/token em campo de input de chat processado por motores de renderização ou scrapers de pré-visualização.

## Conclusão Técnica
Diferente de vulnerabilidades de SSRF puro (onde há exposição de serviços de rede interna), o disparo de tokens por meio de crawlers de plataformas sociais ou de IA demonstra como os sistemas tratam referências externas: validação automatizada de URLs via proxies de borda e indexadores dedicados (`fwdproxy`). Útil para mapear o tempo de resposta e a pegada digital de robôs de indexação corporativos.
