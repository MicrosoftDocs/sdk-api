---
UID: NF:objbase.StgGetIFillLockBytesOnILockBytes
title: StgGetIFillLockBytesOnILockBytes function (objbase.h)
author: windows-sdk-content
description: Creates a new wrapper object on a byte array object provided by the caller.
old-location: stg\stggetifilllockbytesonilockbytes.htm
tech.root: Stg
ms.assetid: 87159472-3b80-4c0f-b2d4-7635dfcf2121
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StgGetIFillLockBytesOnILockBytes, StgGetIFillLockBytesOnILockBytes function [Structured Storage], _stg_stggetifilllockbytesonilockbytes, objbase/StgGetIFillLockBytesOnILockBytes, stg.stggetifilllockbytesonilockbytes
ms.topic: function
f1_keywords: ["objbase/StgGetIFillLockBytesOnILockBytes"]
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
 - StgGetIFillLockBytesOnILockBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StgGetIFillLockBytesOnILockBytes function


## -description


<p class="CCE_Message">[The 
<b>StgGetIFillLockBytesOnILockBytes</b> function is obsolete and the following information is provided for versions of Windows prior to Windows 2000.]

Creates a new wrapper object on a byte array object provided by the caller.


## -parameters




### -param pilb [in]

Pointer to an existing byte array object.


### -param ppflb [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ifilllockbytes">IFillLockBytes</a> pointer variable that receives the interface pointer to the new byte array wrapper object.


## -returns



This function supports the standard return values E_UNEXPECTED and E_FAIL, as well as the following:




## -remarks



The 
<b>StgGetIFillLockBytesOnILockBytes</b> function makes it possible to create an asynchronous storage wrapper object on a custom byte-array object. For example, if you wanted to implement asynchronous storage on a database for which you have already created a byte-array object, you would call this function to create the wrapper object for the byte array. To do so, the function creates a new wrapper object and then initializes it by passing it a pointer to the existing byte-array object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ifilllockbytes">IFillLockBytes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>
 

 

