---
UID: NF:wdspxe.PxePacketAllocate
title: PxePacketAllocate function
author: windows-sdk-content
description: Allocates a packet to be sent with the PxeSendReply function.
old-location: wds\pxepacketallocate.htm
old-project: Wds
ms.assetid: f3a664a8-565c-4894-bea7-6664df0ecd9b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PxePacketAllocate, PxePacketAllocate function [Windows Deployment Services], wds.pxepacketallocate, wdspxe/PxePacketAllocate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WdsPxe.dll
api_name:
-	PxePacketAllocate
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxePacketAllocate function


## -description


Allocates a packet to be sent with the 
    <a href="https://msdn.microsoft.com/b4809f0b-b8a5-45d1-b6ef-8f812379e706">PxeSendReply</a> function.


## -parameters




### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function.


### -param hClientRequest [in]

Handle to the client request received in the 
      <a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a> callback.


### -param uSize [in]

Size of the buffer to be allocated.


## -returns



Address of allocated buffer, or <b>NULL</b> if the allocation failed. For extended error 
      information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/de93d42d-9c46-4944-a6e9-5dd72b8a3278">PxePacketFree</a>



<a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a>



<a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a>



<a href="https://msdn.microsoft.com/b4809f0b-b8a5-45d1-b6ef-8f812379e706">PxeSendReply</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

