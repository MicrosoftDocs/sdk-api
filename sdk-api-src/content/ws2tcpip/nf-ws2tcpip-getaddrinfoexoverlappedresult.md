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

# GetAddrInfoExOverlappedResult function


## -description


The 
<b>GetAddrInfoExOverlappedResult</b> function gets the return code for an <b>OVERLAPPED</b> structure used by an asynchronous operation for the  <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function.


## -parameters




### -param lpOverlapped

A pointer to an <b>OVERLAPPED</b> structure for the asynchronous operation.


## -returns




						On success,  the <b>GetAddrInfoExOverlappedResult</b> function returns <b>NO_ERROR</b> (0). When the
    underlying operation hasn't yet completed, the <b>GetAddrInfoExOverlappedResult</b> function  returns <b>WSAEINPROGRESS</b>. On failure, the <b>GetAddrInfoExOverlappedResult</b> function  returns <b>WSAEINVAL</b>.




## -remarks



The 
<b>GetAddrInfoExOverlappedResult</b> function is used with the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function for asynchronous operations.

If the <b>GetAddrInfoExOverlappedResult</b> function returns <b>WSAEINVAL</b>, the only way to distinguish whether <b>GetAddrInfoExOverlappedResult</b> function or the asynchronous operation returned  the
    error is to check that the <i>lpOverlapped</i> parameter was not NULL. If the <i>lpOverlapped</i> parameter was NULL, then the <b>GetAddrInfoExOverlappedResult</b> function was passed a NULL pointer and failed. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>
 

 

