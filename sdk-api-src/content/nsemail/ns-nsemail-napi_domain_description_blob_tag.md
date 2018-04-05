---
UID: NS:nsemail.napi_domain_description_blob_tag
title: napi_domain_description_blob_tag
author: windows-driver-content
description: Describes a domain handled by a namespace provider for the NS_EMAIL namespace.
old-location: winsock\napi_domain_description_blob.htm
old-project: WinSock
ms.assetid: 543aa20c-eec2-4177-87ed-ba9c91251010
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: NAPI_DOMAIN_DESCRIPTION_BLOB, NAPI_DOMAIN_DESCRIPTION_BLOB structure [Winsock], PNAPI_DOMAIN_DESCRIPTION_BLOB, PNAPI_DOMAIN_DESCRIPTION_BLOB structure pointer [Winsock], napi_domain_description_blob_tag, nsemail/NAPI_DOMAIN_DESCRIPTION_BLOB, nsemail/PNAPI_DOMAIN_DESCRIPTION_BLOB, winsock.napi_domain_description_blob
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NAPI_DOMAIN_DESCRIPTION_BLOB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Nsemail.h
api_name:
-	NAPI_DOMAIN_DESCRIPTION_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# napi_domain_description_blob_tag structure


## -description


The 
<b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure describes a domain handled by a namespace provider for the NS_EMAIL namespace.


## -struct-fields




### -field AuthLevel

The authority level of the namespace provider for this domain. This member can be one of the values from the <a href="https://msdn.microsoft.com/70b5fcde-657b-4f27-b55b-5f5ac3373344">NAPI_PROVIDER_LEVEL</a> enumeration type defined in the <i>Nsemail.h</i> header file. 


### -field cchDomainName

The length, in Unicode characters, of the Unicode string that contains the domain name represented by the <b>OffsetThisDomainName</b> member. The <b>NULL</b> terminator is not counted when calculating the length.


### -field OffsetNextDomainDescription

The offset, in bytes, to the next <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure in the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.


### -field OffsetThisDomainName

The offset, in bytes, to a Unicode string that contains a domain name handled by this namespace provider for the NS_EMAIL namespace. The domain name must be at least <b>cchDomainName</b> Unicode characters in length. <b>NULL</b>-termination of the Unicode string that contains the domain name is recommended, but not required. This offset must be aligned on a minimum of a two-byte boundary.


## -remarks



This structure is supported on Windows Vista
  and later.

The 
<b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure describes a domain handled by a namespace provider for the NS_EMAIL namespace. A typical domain name represented by the <b>OffsetThisDomainName</b> member in this structure might be msn.com or yahoo.com.

Each namespace provider registered in the NS_EMAIL namespace can support multiple domains. The list of supported domains is specified in the provider registration blob as a list of <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures. Each supported domain specification contains a <a href="https://msdn.microsoft.com/70b5fcde-657b-4f27-b55b-5f5ac3373344">NAPI_PROVIDER_LEVEL</a> value in the <b>AuthLevel</b> member of the <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> that describes the type of support provided by the provider for that domain. 

The <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure is a member of the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure used to describe and register a NS_EMAIL namespace provider. There may be multiple <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures in the <b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure for an NS_EMAIL namespace provider.

The <a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a> and <a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

The <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> and <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate all namespace providers (including NS_EMAIL namespace providers) and to retrieve the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure for  a provider if the provider registered a blob upon installation.




## -see-also




<a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://msdn.microsoft.com/70b5fcde-657b-4f27-b55b-5f5ac3373344">NAPI_PROVIDER_LEVEL</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a>



<a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a>
 

 

