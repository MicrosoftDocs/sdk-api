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

# StgIsStorageFile function


## -description


The <b>StgIsStorageFile</b> function indicates whether a particular disk file contains a storage object.


## -parameters




### -param pwcsName [in]

Pointer to the null-terminated Unicode string name of the disk file to be examined. The <i>pwcsName</i> parameter is passed uninterpreted to the underlying file system.


## -returns



<b>StgIsStorageFile</b> function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. See 
<a href="_com_error_handling_strategies">Error Handling Strategies</a> and 
<a href="_com_handling_unknown_errors">Handling Unknown Errors</a>





## -remarks



At the beginning of the disk file underlying a storage object is a signature distinguishing a storage object from other file formats. The 
<b>StgIsStorageFile</b> function is useful to applications whose documents use a disk file format that might or might not use storage objects.

If a root compound file has been created in transacted mode but not yet committed, this method still return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ce0e29fd-1b21-4064-8e37-1a5d5df8bb61">StgIsStorageILockBytes</a>
 

 

