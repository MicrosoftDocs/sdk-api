---
UID: NF:objbase.StgGetIFillLockBytesOnILockBytes
title: StgGetIFillLockBytesOnILockBytes function
author: windows-driver-content
description: Creates a new wrapper object on a byte array object provided by the caller.
old-location: stg\stggetifilllockbytesonilockbytes.htm
old-project: Stg
ms.assetid: 87159472-3b80-4c0f-b2d4-7635dfcf2121
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: StgGetIFillLockBytesOnILockBytes, StgGetIFillLockBytesOnILockBytes function [Structured Storage], _stg_stggetifilllockbytesonilockbytes, objbase/StgGetIFillLockBytesOnILockBytes, stg.stggetifilllockbytesonilockbytes
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
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	StgGetIFillLockBytesOnILockBytes
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
<a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a> pointer variable that receives the interface pointer to the new byte array wrapper object.


## -returns



This function supports the standard return values E_UNEXPECTED and E_FAIL, as well as the following:




## -remarks



The 
<b>StgGetIFillLockBytesOnILockBytes</b> function makes it possible to create an asynchronous storage wrapper object on a custom byte-array object. For example, if you wanted to implement asynchronous storage on a database for which you have already created a byte-array object, you would call this function to create the wrapper object for the byte array. To do so, the function creates a new wrapper object and then initializes it by passing it a pointer to the existing byte-array object.




## -see-also




<a href="https://msdn.microsoft.com/033b3db4-3ff0-4cb4-916f-2490e92f5e6a">IFillLockBytes</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>
 

 

