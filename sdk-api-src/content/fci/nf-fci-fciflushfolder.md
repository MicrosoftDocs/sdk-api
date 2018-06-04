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

# FCIFlushFolder function


## -description


The <b>FCIFlushFolder</b> function forces the current folder under construction to be completed immediately.


## -parameters




### -param hfci [in]

A valid FCI context handle returned by the <a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a> function.


### -param pfnfcignc

TBD


### -param pfnfcis

TBD




#### - GetNextCab [in]

Pointer to an application-defined callback function to obtain specifications on the next cabinet to create. The function should be declared using the <a href="https://msdn.microsoft.com/d56fb63e-91bf-4991-a954-176211697a2e">FNFCIGETNEXTCABINET</a> macro.


#### - pfnProgress [in]

Pointer to an application-defined callback function to update the user. The function should be declared using the <a href="https://msdn.microsoft.com/529fd3c8-9783-4dbe-9268-a9137935cf9b">FNFCISTATUS</a> macro.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, FASLE.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.




## -remarks



The <b>FCIFlushFolder</b> API forces the folder currently under construction to be completed immediately; effectively resetting the compression history if a compression method is in use.

The callback function indicated by <i>GetNextCab</i> will be called if the cabinet overflows, which occurs if the pending data buffered inside an FCI causes the application-specified cabinet media size to be exceeded.




## -see-also




<a href="https://msdn.microsoft.com/dc586260-180e-4a6b-accf-2ddd62ac1335">FCIFlushCabinet</a>
 

 

