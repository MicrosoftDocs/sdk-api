---
UID: NS:ws2spi._WSC_PROVIDER_AUDIT_INFO
title: WSC_PROVIDER_AUDIT_INFO (ws2spi.h)
description: Contains audit information for a layered service provider (LSP) entry in Windows Sockets 2.
helpviewer_keywords: ["PWSC_PROVIDER_AUDIT_INFO","PWSC_PROVIDER_AUDIT_INFO structure pointer [Winsock]","WSC_PROVIDER_AUDIT_INFO","WSC_PROVIDER_AUDIT_INFO structure [Winsock]","winsock.wsc_provider_audit_info","ws2spi/PWSC_PROVIDER_AUDIT_INFO","ws2spi/WSC_PROVIDER_AUDIT_INFO"]
old-location: winsock\wsc_provider_audit_info.htm
tech.root: WinSock
ms.assetid: de2e643f-08d5-4cbb-bd12-843478856011
ms.date: 12/05/2018
ms.keywords: PWSC_PROVIDER_AUDIT_INFO, PWSC_PROVIDER_AUDIT_INFO structure pointer [Winsock], WSC_PROVIDER_AUDIT_INFO, WSC_PROVIDER_AUDIT_INFO structure [Winsock], winsock.wsc_provider_audit_info, ws2spi/PWSC_PROVIDER_AUDIT_INFO, ws2spi/WSC_PROVIDER_AUDIT_INFO
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
req.typenames: WSC_PROVIDER_AUDIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSC_PROVIDER_AUDIT_INFO
 - ws2spi/_WSC_PROVIDER_AUDIT_INFO
 - WSC_PROVIDER_AUDIT_INFO
 - ws2spi/WSC_PROVIDER_AUDIT_INFO
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
 - WSC_PROVIDER_AUDIT_INFO
---

# WSC_PROVIDER_AUDIT_INFO structure


## -description

<div class="alert">**Note**  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a>.</div><div> </div>The 
**WSC_PROVIDER_AUDIT_INFO** structure contains audit information for a layered service provider (LSP) entry in Windows Sockets 2.

## -struct-fields

### -field RecordSize

The size, in bytes of this audit information record which includes this member.

### -field Reserved

A reserved member for the audit information record.

## -remarks

The 
**WSC_PROVIDER_AUDIT_INFO** structure is not currently used.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetproviderinfo">WSCGetProviderInfo</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetproviderinfo32">WSCGetProviderInfo32</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscsetproviderinfo">WSCSetProviderInfo</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscsetproviderinfo32">WSCSetProviderInfo32</a>



<a href="/windows/desktop/api/ws2spi/ne-ws2spi-wsc_provider_info_type">WSC_PROVIDER_INFO_TYPE</a>

