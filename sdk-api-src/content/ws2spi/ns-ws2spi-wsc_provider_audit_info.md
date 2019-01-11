---
UID: NS:ws2spi._WSC_PROVIDER_AUDIT_INFO
title: WSC_PROVIDER_AUDIT_INFO
author: windows-sdk-content
description: Contains audit information for a layered service provider (LSP) entry in Windows Sockets 2.
old-location: winsock\wsc_provider_audit_info.htm
tech.root: WinSock
ms.assetid: de2e643f-08d5-4cbb-bd12-843478856011
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PWSC_PROVIDER_AUDIT_INFO, PWSC_PROVIDER_AUDIT_INFO structure pointer [Winsock], WSC_PROVIDER_AUDIT_INFO, WSC_PROVIDER_AUDIT_INFO structure [Winsock], winsock.wsc_provider_audit_info, ws2spi/PWSC_PROVIDER_AUDIT_INFO, ws2spi/WSC_PROVIDER_AUDIT_INFO
ms.topic: struct
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
 - WSC_PROVIDER_AUDIT_INFO
product: Windows
targetos: Windows
req.typenames: WSC_PROVIDER_AUDIT_INFO
req.redist: 
---

# WSC_PROVIDER_AUDIT_INFO structure


## -description


<div class="alert"><b>Note</b>  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="https://msdn.microsoft.com/0436f559-20e6-4199-8391-10eb7d85df23">Windows Filtering Platform</a>.</div><div> </div>The 
<b>WSC_PROVIDER_AUDIT_INFO</b> structure contains audit information for a layered service provider (LSP) entry in Windows Sockets 2.


## -struct-fields




### -field RecordSize

The size, in bytes of this audit information record which includes this member.


### -field Reserved

A reserved member for the audit information record. 


## -remarks



The 
<b>WSC_PROVIDER_AUDIT_INFO</b> structure is not currently used.




## -see-also




<a href="https://msdn.microsoft.com/5880f3dd-2a74-4af8-b0d8-2a8eedccc1e6">WSCGetProviderInfo</a>



<a href="https://msdn.microsoft.com/91686b38-3cde-4979-8bf6-45e805dd37ff">WSCGetProviderInfo32</a>



<a href="https://msdn.microsoft.com/10eed3e6-d5a0-4ba4-964e-3d924a231afb">WSCSetProviderInfo</a>



<a href="https://msdn.microsoft.com/adb2737f-5327-4306-bd57-f165f339f911">WSCSetProviderInfo32</a>



<a href="https://msdn.microsoft.com/7f93a660-6f53-4e3c-a938-54a13b34258d">WSC_PROVIDER_INFO_TYPE</a>
 

 

