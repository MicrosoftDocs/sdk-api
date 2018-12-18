---
UID: NF:objidl.IFillLockBytes.SetFillSize
title: IFillLockBytes::SetFillSize
author: windows-sdk-content
description: The SetFillSize method sets the expected size of the byte array.
old-location: stg\ifilllockbytes_setfillsize.htm
tech.root: stg
ms.assetid: 1336079e-02d2-4799-a58f-d097ec80c03b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFillLockBytes interface [Structured Storage],SetFillSize method, IFillLockBytes.SetFillSize, IFillLockBytes::SetFillSize, SetFillSize, SetFillSize method [Structured Storage], SetFillSize method [Structured Storage],IFillLockBytes interface, _stg_ifilllockbytes_setfillsize, objidl/IFillLockBytes::SetFillSize, stg.ifilllockbytes_setfillsize
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IFillLockBytes.SetFillSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFillLockBytes::SetFillSize


## -description


The 
<b>SetFillSize</b> method sets the expected size of the byte array.


## -parameters




### -param ulSize [in]

Size in bytes of the byte array object that is to be filled in subsequent calls to 
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a>.


## -returns



This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL.




## -remarks



If 
<b>SetFillSize</b> has not been called, any call to 
<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a> that attempts to access data that has not yet been written using 
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a> or 
<a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">IFillLockBytes::FillAt</a> will return a new error message, E_PENDING. After 
<b>SetFillSize</b> has been called, any call to 
<b>ReadAt</b> that attempts to access data beyond the current size, as set by 
<b>SetFillSize</b>, returns E_FAIL instead of E_PENDING.




## -see-also




<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a>



<a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">IFillLockBytes::FillAt</a>



<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a>
 

 

