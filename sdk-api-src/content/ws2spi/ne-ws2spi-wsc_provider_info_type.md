---
UID: NE:ws2spi._WSC_PROVIDER_INFO_TYPE
title: WSC_PROVIDER_INFO_TYPE (ws2spi.h)
description: Enumeration type is used to specify the information class of a layered service protocol (LSP) in Windows Sockets 2.
helpviewer_keywords: ["ProviderInfoAudit","ProviderInfoLspCategories","WSC_PROVIDER_INFO_TYPE","WSC_PROVIDER_INFO_TYPE enumeration [Winsock]","winsock.wsc_provider_info_type","ws2spi/ProviderInfoAudit","ws2spi/ProviderInfoLspCategories","ws2spi/WSC_PROVIDER_INFO_TYPE"]
old-location: winsock\wsc_provider_info_type.htm
tech.root: WinSock
ms.assetid: 7f93a660-6f53-4e3c-a938-54a13b34258d
ms.date: 12/05/2018
ms.keywords: ProviderInfoAudit, ProviderInfoLspCategories, WSC_PROVIDER_INFO_TYPE, WSC_PROVIDER_INFO_TYPE enumeration [Winsock], winsock.wsc_provider_info_type, ws2spi/ProviderInfoAudit, ws2spi/ProviderInfoLspCategories, ws2spi/WSC_PROVIDER_INFO_TYPE
req.header: ws2spi.h
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
req.typenames: WSC_PROVIDER_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSC_PROVIDER_INFO_TYPE
 - ws2spi/_WSC_PROVIDER_INFO_TYPE
 - WSC_PROVIDER_INFO_TYPE
 - ws2spi/WSC_PROVIDER_INFO_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSC_PROVIDER_INFO_TYPE
---

# WSC_PROVIDER_INFO_TYPE enumeration


## -description

<div class="alert">**Note**  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a>.</div><div> </div>The Windows Sockets 
**WSC_PROVIDER_INFO_TYPE**enumeration type is used to specify the information class of a layered service protocol (LSP) in Windows Sockets 2.

## -enum-fields

### -field ProviderInfoLspCategories

The LSP category information for a protocol entry in a layered protocol. The information class should point to a DWORD value containing the appropriate LSP category flags implemented by LSP.

### -field ProviderInfoAudit

The LSP class information for audit information for the LSP entry. The information class should point to a <a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsc_provider_audit_info">WSC_PROVIDER_AUDIT_INFO</a> structure containing an audit record for the LSP.

## -remarks

The 
<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsc_provider_audit_info">WSC_PROVIDER_AUDIT_INFO</a> structure is not currently used.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetproviderinfo">WSCGetProviderInfo</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetproviderinfo32">WSCGetProviderInfo32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscsetproviderinfo">WSCSetProviderInfo</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscsetproviderinfo32">WSCSetProviderInfo32</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsc_provider_audit_info">WSC_PROVIDER_AUDIT_INFO</a>

