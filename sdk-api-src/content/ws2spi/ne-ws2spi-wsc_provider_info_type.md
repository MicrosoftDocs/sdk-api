---
UID: NE:ws2spi._WSC_PROVIDER_INFO_TYPE
title: WSC_PROVIDER_INFO_TYPE (ws2spi.h)
author: windows-sdk-content
description: Enumeration type is used to specify the information class of a layered service protocol (LSP) in Windows Sockets 2.
old-location: winsock\wsc_provider_info_type.htm
tech.root: WinSock
ms.assetid: 7f93a660-6f53-4e3c-a938-54a13b34258d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ProviderInfoAudit, ProviderInfoLspCategories, WSC_PROVIDER_INFO_TYPE, WSC_PROVIDER_INFO_TYPE enumeration [Winsock], winsock.wsc_provider_info_type, ws2spi/ProviderInfoAudit, ws2spi/ProviderInfoLspCategories, ws2spi/WSC_PROVIDER_INFO_TYPE
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSC_PROVIDER_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: WSC_PROVIDER_INFO_TYPE
req.redist: 
---

# WSC_PROVIDER_INFO_TYPE enumeration


## -description


<div class="alert"><b>Note</b>  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="https://msdn.microsoft.com/0436f559-20e6-4199-8391-10eb7d85df23">Windows Filtering Platform</a>.</div><div> </div>The Windows Sockets 
<b>WSC_PROVIDER_INFO_TYPE</b>enumeration type is used to specify the information class of a layered service protocol (LSP) in Windows Sockets 2.


## -enum-fields




### -field ProviderInfoLspCategories

The LSP category information for a protocol entry in a layered protocol. The information class should point to a DWORD value containing the appropriate LSP category flags implemented by LSP.


### -field ProviderInfoAudit

The LSP class information for audit information for the LSP entry. The information class should point to a <a href="https://msdn.microsoft.com/de2e643f-08d5-4cbb-bd12-843478856011">WSC_PROVIDER_AUDIT_INFO</a> structure containing an audit record for the LSP.


## -remarks



The 
<a href="https://msdn.microsoft.com/de2e643f-08d5-4cbb-bd12-843478856011">WSC_PROVIDER_AUDIT_INFO</a> structure is not currently used.




## -see-also




<a href="https://msdn.microsoft.com/5880f3dd-2a74-4af8-b0d8-2a8eedccc1e6">WSCGetProviderInfo</a>



<a href="https://msdn.microsoft.com/91686b38-3cde-4979-8bf6-45e805dd37ff">WSCGetProviderInfo32</a>



<a href="https://msdn.microsoft.com/10eed3e6-d5a0-4ba4-964e-3d924a231afb">WSCSetProviderInfo</a>



<a href="https://msdn.microsoft.com/adb2737f-5327-4306-bd57-f165f339f911">WSCSetProviderInfo32</a>



<a href="https://msdn.microsoft.com/de2e643f-08d5-4cbb-bd12-843478856011">WSC_PROVIDER_AUDIT_INFO</a>
 

 

