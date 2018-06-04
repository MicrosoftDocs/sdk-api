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

# NetFreeAadJoinInformation function


## -description


Frees the memory allocated for the specified <a href="https://msdn.microsoft.com/9B0F7BE3-BDCD-437E-9157-9A646A2A20E2">DSREG_JOIN_INFO</a> structure, which contains join information for a tenant and which you retrieved by calling the <a href="https://msdn.microsoft.com/C63B3AA7-FC7E-4CB9-9318-BD25560591AB">NetGetAadJoinInformation</a> function.


## -parameters




### -param pJoinInfo [in, optional]

Pointer to the <a href="https://msdn.microsoft.com/9B0F7BE3-BDCD-437E-9157-9A646A2A20E2">DSREG_JOIN_INFO</a> structure for which you want to free the memory. 


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/9B0F7BE3-BDCD-437E-9157-9A646A2A20E2">DSREG_JOIN_INFO</a>



<a href="https://msdn.microsoft.com/C63B3AA7-FC7E-4CB9-9318-BD25560591AB">NetGetAadJoinInformation</a>
 

 

