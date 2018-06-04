---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WSC_PROVIDER_AUDIT_INFO structure


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
 

 

