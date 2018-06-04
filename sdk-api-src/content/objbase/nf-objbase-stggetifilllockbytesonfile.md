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

# StgGetIFillLockBytesOnFile function


## -description


<p class="CCE_Message">[The <b>StgGetIFillLockBytesOnFile</b>  function is obsolete. The following information is provided to support versions of Windows prior to Windows 2000.]

The <b>StgGetIFillLockBytesOnFile</b>  function opens a wrapper object on a temporary file.


## -parameters




### -param pwcsName [in]

A pointer to the null-terminated unicode string name of the file for which a wrapper object is created.


### -param ppflb [out]

A pointer to 
<a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a>* pointer variable that receives the interface pointer to the new byte array wrapper object.


## -returns




						This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, in addition to the following:

The <b>StgGetIFillLockBytesOnFile</b>  function can also return any file system errors.




## -remarks



The moniker that manages the downloading of the file specified in <i>pwcsName</i> calls this function in the course of creating the asynchronous storage necessary to manage the asynchronous downloading of data. The moniker first creates a temporary file, then calls this function to create the wrapper object on that file. Finally, the moniker calls 
<a href="https://msdn.microsoft.com/6772b669-b311-4b7d-8873-44fadbecdec7">StgOpenAsyncDocfileOnIFillLockBytes</a> to open the root storage of the compound file to be downloaded into the temporary file.




## -see-also




<a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/6772b669-b311-4b7d-8873-44fadbecdec7">StgOpenAsyncDocfileOnIFillLockBytes</a>
 

 

