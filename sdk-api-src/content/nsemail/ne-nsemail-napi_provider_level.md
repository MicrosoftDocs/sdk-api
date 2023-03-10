---
UID: NE:nsemail.napi_provider_level_tag
title: NAPI_PROVIDER_LEVEL (nsemail.h)
description: Specifies the provider authority level of a NS_EMAIL namespace provider for a given domain.
helpviewer_keywords: ["NAPI_PROVIDER_LEVEL","NAPI_PROVIDER_LEVEL enumeration [Winsock]","ProviderLevel_None","ProviderLevel_Primary","ProviderLevel_Secondary","nsemail/NAPI_PROVIDER_LEVEL","nsemail/ProviderLevel_None","nsemail/ProviderLevel_Primary","nsemail/ProviderLevel_Secondary","winsock.napi_provider_level"]
old-location: winsock\napi_provider_level.htm
tech.root: WinSock
ms.assetid: 70b5fcde-657b-4f27-b55b-5f5ac3373344
ms.date: 12/05/2018
ms.keywords: NAPI_PROVIDER_LEVEL, NAPI_PROVIDER_LEVEL enumeration [Winsock], ProviderLevel_None, ProviderLevel_Primary, ProviderLevel_Secondary, nsemail/NAPI_PROVIDER_LEVEL, nsemail/ProviderLevel_None, nsemail/ProviderLevel_Primary, nsemail/ProviderLevel_Secondary, winsock.napi_provider_level
req.header: nsemail.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NAPI_PROVIDER_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - napi_provider_level_tag
 - nsemail/napi_provider_level_tag
 - NAPI_PROVIDER_LEVEL
 - nsemail/NAPI_PROVIDER_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nsemail.h
api_name:
 - NAPI_PROVIDER_LEVEL
---

# NAPI_PROVIDER_LEVEL enumeration


## -description

The <b>NAPI_PROVIDER_LEVEL</b> enumeration specifies the provider authority level of a  NS_EMAIL namespace provider for a given domain.

## -enum-fields

### -field ProviderLevel_None:0

The namespace provider does not support the current domain. This value can be used to temporarily turn off the support for a domain without removing it from the list of supported domains. 

If <b>ProviderLevel_None</b> is set in the <b>AuthLevel</b> member of the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_domain_description_blob">NAPI_DOMAIN_DESCRIPTION_BLOB</a> for a given domain when the provider is installed and registered, the namespace provider will not be called to resolve or register an address in that domain unless the provider registered as a wildcard provider. 

There may be multiple NS_EMAIL namespace providers for a domain with a value of <b>ProviderLevel_None</b>. If there are namespace providers with this value that also registered as a wildcard provider, the providers are called in the order that they appear in the Winsock catalog.

### -field ProviderLevel_Secondary

The namespace provider is a secondary provider for a domain in the NS_EMAIL namespace. A namespace provider can be a secondary provider in the target domain if the provider can resolve and register NS_EMAIL names for this domain and give the same answer that a primary provider would provide. If <b>ProviderLevel_Secondary</b> is set in <b>AuthLevel</b> member of the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_domain_description_blob">NAPI_DOMAIN_DESCRIPTION_BLOB</a> for a given domain when the provider is installed and registered, this provider is called when a primary provider for the domain is not currently available or the primary provider could not resolve or register the address in that domain. 

There may be multiple secondary NS_EMAIL namespace providers for a domain with a value of <b>ProviderLevel_Secondary</b>. If there are multiple secondary namespace providers, the providers are called in the order that they appear in the Winsock catalog.

### -field ProviderLevel_Primary

The namespace provider is the primary provider for a domain in the NS_EMAIL namespace. A namespace provider can claim to be the primary provider for a domain if it owns all of the NS_EMAIL names for that domain and thus has access to the master data for all such names. 

There should be only a single primary NS_EMAIL namespace provider for a domain registered on the local system.

<div class="alert"><b>Note</b>  There should never be two NS_EMAIL namespace providers that claim to be the primary provider for the same domain. If multiple providers try to register as the primary provider for the same domain, the first provider found in the Winsock namespace catalog for the domain as the primary provider will be called. All other provider claims to be the primary provider are ignored.</div>
<div> </div>

## -remarks

This enumeration is supported on Windows Vista and later.

The <b>NAPI_PROVIDER_LEVEL</b> enumeration is used by the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_domain_description_blob">NAPI_DOMAIN_DESCRIPTION_BLOB</a> structure to specify the authority level of  a NS_EMAIL namespace provider for a domain. Each namespace provider registered in the NS_EMAIL namespace can support multiple domains. The list of supported domains is specified in the provider registration blob as a list of <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures. Each supported domain specification contains a <b>NAPI_PROVIDER_LEVEL</b> value in the <b>AuthLevel</b> member of the <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> that describes the type of support provided by the provider for that domain. 

In addition to the specified domain, a NS_EMAIL namespace provider can also register as a wildcard provider to try and support any domain, by specifying the <b>fSupportsWildCard</b> member as nonzero in the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> passed when the provider is installed.

Namespace providers are called in the following order to resolve or register an address in a domain. If a namespace provider registered as the primary provider for the domain, then this primary provider is called first. There are two cases depending on whether authoritative results are requested in the namespace query. The default for a query is to request authoritative results.

 When authoritative results are requested in the query, then namespace providers are called as follows. If the primary provider is unavailable or is unable to resolve or register the address, then the first  secondary provider in the Winsock catalog is called. If the secondary provider is unavailable or is unable to resolve or register the address, then the next secondary provider in the Winsock catalog is called. If all of the secondary providers are unavailable or are unable to resolve or register the address, then the first wildcard provider in the Winsock catalog is called. If the first wildcard provider is unavailable or is unable to resolve or register the address, then the next wildcard provider in the Winsock catalog is called.

 When non-authoritative results are requested in the query, then namespace providers are called as follows. The primary provider, all secondary providers, and all wildcard providers are called and results from all of the queries are returned.  The primary provider is called first. Secondary providers are called next, based on the order in the Winsock catalog. Wildcard providers are called next, based on the order in the Winsock catalog. The results that are returned are based on the order of the queries.

The <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_domain_description_blob">NAPI_DOMAIN_DESCRIPTION_BLOB</a> structure is used in the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure to describe a NS_EMAIL namespace provider. 

The <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate namespace providers for the NS_EMAIL namespace and retrieve the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure for  a provider.

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_domain_description_blob">NAPI_DOMAIN_DESCRIPTION_BLOB</a>



<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a>
