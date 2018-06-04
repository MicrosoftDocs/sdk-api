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

# FCIFlushCabinet function


## -description


The <b>FCIFlushCabinet</b> function completes the current cabinet.


## -parameters




### -param hfci [in]

A valid FCI context handle returned by the<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a> function.


### -param fGetNextCab [in]

Specifies whether the function pointed to by the supplied <i>GetNextCab</i> parameter will be called.


### -param pfnfcignc

TBD


### -param pfnfcis

TBD




#### - GetNextCab [in]

Pointer to an application-defined callback function to obtain specifications on the next cabinet to create. The function should be declared using the <a href="https://msdn.microsoft.com/d56fb63e-91bf-4991-a954-176211697a2e">FNFCIGETNEXTCABINET</a> macro.


#### - pfnProgress [in]

Pointer to an application-defined callback function to update the user. The function should be declared using the <a href="https://msdn.microsoft.com/529fd3c8-9783-4dbe-9268-a9137935cf9b">FNFCISTATUS</a> macro.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.




## -remarks



The <b>FCIFlushCabinet</b> API forces the current cabinet under construction to be completed immediately and then written to disk. Further calls to <a href="https://msdn.microsoft.com/f99e8718-853b-4d35-98ae-61a8333dbaba">FCIAddFile</a> will result in files being added to another cabinet.

 In the event the current cabinet has reached the application-specified media size limit, the pending data within an FCI's internal buffers will be placed into another cabinet.

The <i>fGetNextCab</i> flag determines whether the function pointed to by the <i>GetNextCab</i> parameter will be called. If <i>fGetNextCab</i> is set <b>TRUE</b>, <i>GetNextCab</i> is called to obtain continuation information. If <b>FALSE</b>, then <i>GetNextCab</i> is called only in the event the cabinet overflows.




## -see-also




<a href="https://msdn.microsoft.com/dc9c226e-e309-48c3-9edb-3f0a040c0c18">FCIFlushFolder</a>
 

 

