---
UID: NF:drt.DrtUnregisterKey
title: DrtUnregisterKey function
author: windows-sdk-content
description: The DrtUnregisterKey function deregisters a key from the DRT.
old-location: p2p\drtunregisterkey.htm
tech.root: P2PSdk
ms.assetid: cf8f877b-44a8-4153-bf02-0b0061bc53d2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DrtUnregisterKey, DrtUnregisterKey function [Peer Networking], drt/DrtUnregisterKey, p2p.drtunregisterkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtUnregisterKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrtUnregisterKey function


## -description


The <b>DrtUnregisterKey</b> function deregisters a key from the DRT.


## -parameters




### -param hKeyRegistration [in]

The DRT handle returned by the <a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a> function specifying a registered key within the DRT.


## -returns



This function does not return a value.




## -remarks



A node can deregister a key anytime after registration.  Additionally, if an application calls <a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>, all keys are deregistered by the DRT infrastructure.

Only the application that registered they key may deregister it. An application can deregister a key from the local node. Upon completion the function triggers a <b>DRT_EVENT_LEAFSET_KEY_CHANGE</b> event;  informing the application and other nodes participating in the DRT mesh of the deregistration. 




## -see-also




<a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>



<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>
 

 

