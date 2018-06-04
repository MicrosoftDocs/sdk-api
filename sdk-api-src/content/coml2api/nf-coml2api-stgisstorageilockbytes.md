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

# StgIsStorageILockBytes function


## -description


The <b>StgIsStorageILockBytes</b> function indicates whether the specified byte array contains a storage object.


## -parameters




### -param plkbyt


<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> pointer to the byte array to be examined.


## -returns



This function can also return any file system errors, or system errors wrapped in an <b>HRESULT</b>, or 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface error return values. See 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>





## -remarks



At the beginning of the byte array underlying a storage object is a signature distinguishing a storage object (supporting the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface) from other file formats. The 
<b>StgIsStorageILockBytes</b> function is useful to applications whose documents use a byte array (a byte array object supports the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface) that might or might not use storage objects.




## -see-also




<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/6a0d2da5-4d5c-4da7-9ea6-3b52cd6673fc">StgIsStorageFile</a>
 

 

