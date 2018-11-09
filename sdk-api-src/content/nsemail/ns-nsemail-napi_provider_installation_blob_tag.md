---
UID: NS:nsemail.napi_provider_installation_blob_tag
title: napi_provider_installation_blob_tag
author: windows-sdk-content
description: Contains the information required to install a namespace provider for the NS_EMAIL namespace.
old-location: winsock\napi_provider_installation_blob.htm
tech.root: winsock
ms.assetid: 3444ad63-444a-481d-8fe7-f40b2b7d5283
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: NAPI_PROVIDER_INSTALLATION_BLOB, NAPI_PROVIDER_INSTALLATION_BLOB structure [Winsock], PNAPI_PROVIDER_INSTALLATION_BLOB, PNAPI_PROVIDER_INSTALLATION_BLOB structure pointer [Winsock], napi_provider_installation_blob_tag, nsemail/NAPI_PROVIDER_INSTALLATION_BLOB, nsemail/PNAPI_PROVIDER_INSTALLATION_BLOB, winsock.napi_provider_installation_blob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nsemail.h
api_name:
 - NAPI_PROVIDER_INSTALLATION_BLOB
product: Windows
targetos: Windows
req.typenames: NAPI_PROVIDER_INSTALLATION_BLOB
req.redist: 
---

# napi_provider_installation_blob_tag structure


## -description


The 
<b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure contains the information required to install a namespace provider for the NS_EMAIL namespace.


## -struct-fields




### -field dwVersion

Type: <b>DWORD</b>

The version number of the NS_EMAIL namespace provider. This member is specific to the namespace provider.


### -field dwProviderType

Type: <b>DWORD</b>

The type of namespace provider for the NS_EMAIL namespace. This member can be one of the values from the <a href="https://msdn.microsoft.com/0d845cc5-a84a-43fe-b9e7-d1a9153bae73">NAPI_PROVIDER_TYPE</a> enumeration type defined in the <i>Nsemail.h</i> header file. 


### -field fSupportsWildCard

Type: <b>DWORD</b>

A Boolean value that indicates if this NS_EMAIL namespace provider supports wildcard names. If this member is nonzero, then an NS_EMAIL provider claims to be potentially able to resolve or register any name that does not belong to any domains the provider is specifically registered for as primary or secondary. If this member is nonzero, then the NS_EMAIL provider may be called to resolve or register any address, if  no primary or secondary provider for the domain is available. 

There may be multiple providers that claim to be able to resolve any address (the <b>fSupportsWildCard</b> set to nonzero). If there are namespace providers with this value that also registered as a wildcard provider, the providers are called in the order that they appear in the Winsock namespace catalog.


### -field cDomains

Type: <b>DWORD</b>

The number of <a href="https://msdn.microsoft.com/543aa20c-eec2-4177-87ed-ba9c91251010">NAPI_DOMAIN_DESCRIPTION_BLOB</a> structures the starting at the <b>OffsetFirstDomain</b> member used to describe domains that are supported by this NS_EMAIL namespace provider.


### -field OffsetFirstDomain

Type: <b>DWORD</b>

The offset,  in bytes, to the first of multiple <a href="https://msdn.microsoft.com/543aa20c-eec2-4177-87ed-ba9c91251010">NAPI_DOMAIN_DESCRIPTION_BLOB</a> structures used to describe domains that are supported by this NS_EMAIL namespace provider. This offset must be aligned on a minimum of a four-byte boundary.


## -remarks



This structure is supported on Windows Vistaand later.

The 
<b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure contains the information required to install a namespace provider for the NS_EMAIL namespace. There may be multiple namespace providers for the NS_EMAIL namespace install on a local system.

Each namespace provider registered in the NS_EMAIL namespace can support multiple domains. As a result, there may be multiple <a href="https://msdn.microsoft.com/543aa20c-eec2-4177-87ed-ba9c91251010">NAPI_DOMAIN_DESCRIPTION_BLOB</a> structures in the <b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure for an NS_EMAIL namespace provider. The list of supported domains is specified in the provider registration blob as a list of <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures. Each supported domain specification contains a <a href="https://msdn.microsoft.com/70b5fcde-657b-4f27-b55b-5f5ac3373344">NAPI_PROVIDER_LEVEL</a> value in the <b>AuthLevel</b> member of the <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> that describes the level of authority provided by the provider for that domain. 

Namespace providers are called in the following order to resolve or register an address in a domain. If a namespace provider registered as the primary provider for the domain, then this primary provider is called first. There are two cases depending on whether authoritative results are requested in the namespace query. The default for a query is to request authoritative results.

 When authoritative results are requested in the query, then namespace providers are called as follows. If the primary provider is unavailable or is unable to resolve or register the address, then the first  secondary provider in the Winsock catalog is called. If the secondary provider is unavailable or is unable to resolve or register the address, then the next secondary provider in the Winsock catalog is called. If all of the secondary providers are unavailable or are unable to resolve or register the address, then the first wildcard provider in the Winsock catalog is called. If the first wildcard provider is unavailable or is unable to resolve or register the address, then the next wildcard provider in the Winsock catalog is called.

 When non-authoritative results are requested in the query, then namespace providers are called as follows. The primary provider, all secondary providers, and all wildcard providers are called and results from all of the queries are returned.  The primary provider is called first. Secondary providers are called next, based on the order in the Winsock catalog. Wildcard providers are called next, based on the order in the Winsock catalog. The results that are returned are based on the order of the queries.

The <a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a> and <a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure.  

The <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> and <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate all namespace providers (including NS_EMAIL namespace providers) and to retrieve the <b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure for  a provider if the provider registered a blob upon installation.




## -see-also




<a href="https://msdn.microsoft.com/543aa20c-eec2-4177-87ed-ba9c91251010">NAPI_DOMAIN_DESCRIPTION_BLOB</a>



<a href="https://msdn.microsoft.com/70b5fcde-657b-4f27-b55b-5f5ac3373344">NAPI_PROVIDER_LEVEL</a>



<a href="https://msdn.microsoft.com/0d845cc5-a84a-43fe-b9e7-d1a9153bae73">NAPI_PROVIDER_TYPE</a>



<a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a>



<a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a>
 

 

