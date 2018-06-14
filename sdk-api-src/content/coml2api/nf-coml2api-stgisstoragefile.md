---
UID: NF:coml2api.StgIsStorageFile
title: StgIsStorageFile function
author: windows-sdk-content
description: The StgIsStorageFile function indicates whether a particular disk file contains a storage object.
old-location: stg\stgisstoragefile.htm
old-project: Stg
ms.assetid: 6a0d2da5-4d5c-4da7-9ea6-3b52cd6673fc
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: StgIsStorageFile, StgIsStorageFile function [Structured Storage], _stg_stgisstoragefile, coml2api/StgIsStorageFile, stg.stgisstoragefile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: coml2api.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgIsStorageFile
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# StgIsStorageFile function


## -description


The <b>StgIsStorageFile</b> function indicates whether a particular disk file contains a storage object.


## -parameters




### -param pwcsName [in]

Pointer to the null-terminated Unicode string name of the disk file to be examined. The <i>pwcsName</i> parameter is passed uninterpreted to the underlying file system.


## -returns



<b>StgIsStorageFile</b> function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. See 
<a href="https://docs.microsoft.com/windows/desktop//com/error-handling-strategies">Error Handling Strategies</a> and 
<a href="https://docs.microsoft.com/windows/desktop//com/handling-unknown-errors">Handling Unknown Errors</a>





## -remarks



At the beginning of the disk file underlying a storage object is a signature distinguishing a storage object from other file formats. The 
<b>StgIsStorageFile</b> function is useful to applications whose documents use a disk file format that might or might not use storage objects.

If a root compound file has been created in transacted mode but not yet committed, this method still return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ce0e29fd-1b21-4064-8e37-1a5d5df8bb61">StgIsStorageILockBytes</a>
 

 

