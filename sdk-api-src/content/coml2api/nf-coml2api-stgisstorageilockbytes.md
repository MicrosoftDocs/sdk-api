---
UID: NF:coml2api.StgIsStorageILockBytes
title: StgIsStorageILockBytes function
author: windows-sdk-content
description: The StgIsStorageILockBytes function indicates whether the specified byte array contains a storage object.
old-location: stg\stgisstorageilockbytes.htm
old-project: stg
ms.assetid: ce0e29fd-1b21-4064-8e37-1a5d5df8bb61
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: StgIsStorageILockBytes, StgIsStorageILockBytes function [Structured Storage], _stg_stgisstorageilockbytes, coml2api/StgIsStorageILockBytes, stg.stgisstorageilockbytes
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
 - StgIsStorageILockBytes
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
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
<a href="https://msdn.microsoft.com/library/ms688560(v=VS.85).aspx">Error Handling Strategies</a> and 
<a href="https://msdn.microsoft.com/library/ms693442(v=VS.85).aspx">Handling Unknown Errors</a>





## -remarks



At the beginning of the byte array underlying a storage object is a signature distinguishing a storage object (supporting the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface) from other file formats. The 
<b>StgIsStorageILockBytes</b> function is useful to applications whose documents use a byte array (a byte array object supports the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface) that might or might not use storage objects.




## -see-also




<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/6a0d2da5-4d5c-4da7-9ea6-3b52cd6673fc">StgIsStorageFile</a>
 

 

