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

# WlanFreeMemory function


## -description


The <b>WlanFreeMemory</b> function frees memory.  Any memory returned from Native Wifi functions must be freed.


## -parameters




### -param pMemory [in]

Pointer to the memory to be freed.


## -returns



None.




## -remarks



If <i>pMemory</i> points to memory that has already been freed, an access violation or heap corruption may occur.

There is a hotfix available for  Wireless LAN API for Windows XP with Service Pack 2 (SP2) that can help improve the performance of applications that call <b>WlanFreeMemory</b> and <a href="https://msdn.microsoft.com/27353a1b-2a3c-4c3b-b512-917d010ee8dd">WlanGetAvailableNetworkList</a> many times. For more information, see Help and Knowledge Base article 940541, entitled "FIX: The private bytes of the application continuously increase when an application calls the WlanGetAvailableNetworkList function and the WlanFreeMemory function on a Windows XP Service Pack 2-based computer", in the Help and Support Knowledge Base at <a href="http://go.microsoft.com/fwlink/p/?linkid=102216">http://go.microsoft.com/fwlink/p/?linkid=102216</a>.






## -see-also




<a href="https://msdn.microsoft.com/29200450-4ec8-418d-b633-1ea688755711">WlanAllocateMemory</a>
 

 

