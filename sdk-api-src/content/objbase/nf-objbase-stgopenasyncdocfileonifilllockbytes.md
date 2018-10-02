---
UID: NF:objbase.StgOpenAsyncDocfileOnIFillLockBytes
title: StgOpenAsyncDocfileOnIFillLockBytes function
author: windows-sdk-content
description: Opens an existing root asynchronous storage object on a byte-array wrapper object provided by the caller.
old-location: stg\stgopenasyncdocfileonifilllockbytes.htm
tech.root: Stg
ms.assetid: 6772b669-b311-4b7d-8873-44fadbecdec7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: StgOpenAsyncDocfileOnIFillLockBytes, StgOpenAsyncDocfileOnIFillLockBytes function [Structured Storage], _stg_stgopenasyncdocfileonifilllockbytes, objbase/StgOpenAsyncDocfileOnIFillLockBytes, stg.stgopenasyncdocfileonifilllockbytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - StgOpenAsyncDocfileOnIFillLockBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StgOpenAsyncDocfileOnIFillLockBytes function


## -description


<p class="CCE_Message">[The <b>StgOpenAsyncDocfileOnIFillLockBytes</b> function is obsolete. The following information is provided to support  versions of Windows prior to Windows 2000.]

The <b>StgOpenAsyncDocfileOnIFillLockBytes</b>opens an existing root asynchronous storage object on a byte-array wrapper object provided by the caller.


## -parameters




### -param pflb [in]

A <a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a> pointer to the byte-array wrapper object that contains the storage object to be opened.


### -param grfMode [in]

A value that specifies the access mode to use to open the storage object. The most common access mode, taken from <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>, is STGM_READ.


### -param asyncFlags [in]

A value that indicates whether a connection point on a storage is inherited by its substorages and streams. ASYNC_MODE_COMPATIBILITY indicates that the connection point is inherited; ASYNC_MODE_DEFAULT indicates that the connection point is not inherited.


### -param ppstgOpen [out]

A pointer to 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>* pointer variable that receives the interface pointer to the root asynchronous storage object.


## -returns



This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:




## -remarks



The root storage of the asynchronous storage object is opened according to the access mode in the <i>grfMode</i> parameter. A pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the opened storage object is supplied through the <i>ppstgOpen</i> parameter.

The byte array wrapper object must have been previously instantiated through a call to the 
<a href="https://msdn.microsoft.com/948724ff-d1eb-43ca-b498-6296909cfb28">StgGetIFillLockBytesOnFile</a> function.

<b>StgOpenAsyncDocfileOnIFillLockBytes</b> does not support priority access mode or exclusions. Otherwise, it works in much the same way as the 
<a href="https://msdn.microsoft.com/7920bd46-0a8f-42e0-9988-59d85edb64e2">StgOpenStorageOnILockBytes</a> function.

The returned storage object has a connection point for 
<a href="https://msdn.microsoft.com/en-us/library/ms680740(v=VS.85).aspx">IProgressNotify</a>.




## -see-also




<a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="https://msdn.microsoft.com/948724ff-d1eb-43ca-b498-6296909cfb28">StgGetIFillLockBytesOnFile</a>



<a href="https://msdn.microsoft.com/7920bd46-0a8f-42e0-9988-59d85edb64e2">StgOpenStorageOnILockBytes</a>
 

 

