---
UID: NS:nsemail.napi_domain_description_blob_tag
title: NAPI_DOMAIN_DESCRIPTION_BLOB (nsemail.h)
description: Describes a domain handled by a namespace provider for the NS_EMAIL namespace.
helpviewer_keywords: ["NAPI_DOMAIN_DESCRIPTION_BLOB","NAPI_DOMAIN_DESCRIPTION_BLOB structure [Winsock]","PNAPI_DOMAIN_DESCRIPTION_BLOB","PNAPI_DOMAIN_DESCRIPTION_BLOB structure pointer [Winsock]","nsemail/NAPI_DOMAIN_DESCRIPTION_BLOB","nsemail/PNAPI_DOMAIN_DESCRIPTION_BLOB","winsock.napi_domain_description_blob"]
old-location: winsock\napi_domain_description_blob.htm
tech.root: WinSock
ms.assetid: 543aa20c-eec2-4177-87ed-ba9c91251010
ms.date: 12/05/2018
ms.keywords: NAPI_DOMAIN_DESCRIPTION_BLOB, NAPI_DOMAIN_DESCRIPTION_BLOB structure [Winsock], PNAPI_DOMAIN_DESCRIPTION_BLOB, PNAPI_DOMAIN_DESCRIPTION_BLOB structure pointer [Winsock], nsemail/NAPI_DOMAIN_DESCRIPTION_BLOB, nsemail/PNAPI_DOMAIN_DESCRIPTION_BLOB, winsock.napi_domain_description_blob
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
req.typenames: NAPI_DOMAIN_DESCRIPTION_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - napi_domain_description_blob_tag
 - nsemail/napi_domain_description_blob_tag
 - NAPI_DOMAIN_DESCRIPTION_BLOB
 - nsemail/NAPI_DOMAIN_DESCRIPTION_BLOB
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
 - NAPI_DOMAIN_DESCRIPTION_BLOB
---

# NAPI_DOMAIN_DESCRIPTION_BLOB structure


## -description

The 
<b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure describes a domain handled by a namespace provider for the NS_EMAIL namespace.

## -struct-fields

### -field AuthLevel

The authority level of the namespace provider for this domain. This member can be one of the values from the <a href="/windows/desktop/api/nsemail/ne-nsemail-napi_provider_level">NAPI_PROVIDER_LEVEL</a> enumeration type defined in the <i>Nsemail.h</i> header file.

### -field cchDomainName

The length, in Unicode characters, of the Unicode string that contains the domain name represented by the <b>OffsetThisDomainName</b> member. The <b>NULL</b> terminator is not counted when calculating the length.

### -field OffsetNextDomainDescription

The offset, in bytes, to the next <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure in the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.

### -field OffsetThisDomainName

The offset, in bytes, to a Unicode string that contains a domain name handled by this namespace provider for the NS_EMAIL namespace. The domain name must be at least <b>cchDomainName</b> Unicode characters in length. <b>NULL</b>-termination of the Unicode string that contains the domain name is recommended, but not required. This offset must be aligned on a minimum of a two-byte boundary.

## -remarks

This structure is supported on Windows Vista and later.

The 
<b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure describes a domain handled by a namespace provider for the NS_EMAIL namespace. A typical domain name represented by the <b>OffsetThisDomainName</b> member in this structure might be msn.com or yahoo.com.

Each namespace provider registered in the NS_EMAIL namespace can support multiple domains. The list of supported domains is specified in the provider registration blob as a list of <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures. Each supported domain specification contains a <a href="/windows/desktop/api/nsemail/ne-nsemail-napi_provider_level">NAPI_PROVIDER_LEVEL</a> value in the <b>AuthLevel</b> member of the <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> that describes the type of support provided by the provider for that domain. 

The <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structure is a member of the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure used to describe and register a NS_EMAIL namespace provider. There may be multiple <b>NAPI_DOMAIN_DESCRIPTION_BLOB</b> structures in the <b>NAPI_PROVIDER_INSTALLATION_BLOB</b> structure for an NS_EMAIL namespace provider.

The <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a> functions are used to install a namespace provider for the NS_EMAIL namespace using a <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure. 

The <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a> and <a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a> functions are used to enumerate all namespace providers (including NS_EMAIL namespace providers) and to retrieve the <a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure for  a provider if the provider registered a blob upon installation.

## -see-also

<a href="/windows/desktop/api/nsemail/ns-nsemail-napi_provider_installation_blob">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="/windows/desktop/api/nsemail/ne-nsemail-napi_provider_level">NAPI_PROVIDER_LEVEL</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumnamespaceprovidersexa">WSAEnumNameSpaceProvidersEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32">WSCEnumNameSpaceProvidersEx32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex">WSCInstallNameSpaceEx</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallnamespaceex32">WSCInstallNameSpaceEx32</a>