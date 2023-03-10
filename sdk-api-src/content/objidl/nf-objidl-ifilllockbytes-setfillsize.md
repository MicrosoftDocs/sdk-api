---
UID: NF:objidl.IFillLockBytes.SetFillSize
title: IFillLockBytes::SetFillSize (objidl.h)
description: The SetFillSize method sets the expected size of the byte array.
helpviewer_keywords: ["IFillLockBytes interface [Structured Storage]","SetFillSize method","IFillLockBytes.SetFillSize","IFillLockBytes::SetFillSize","SetFillSize","SetFillSize method [Structured Storage]","SetFillSize method [Structured Storage]","IFillLockBytes interface","_stg_ifilllockbytes_setfillsize","objidl/IFillLockBytes::SetFillSize","stg.ifilllockbytes_setfillsize"]
old-location: stg\ifilllockbytes_setfillsize.htm
tech.root: Stg
ms.assetid: 1336079e-02d2-4799-a58f-d097ec80c03b
ms.date: 12/05/2018
ms.keywords: IFillLockBytes interface [Structured Storage],SetFillSize method, IFillLockBytes.SetFillSize, IFillLockBytes::SetFillSize, SetFillSize, SetFillSize method [Structured Storage], SetFillSize method [Structured Storage],IFillLockBytes interface, _stg_ifilllockbytes_setfillsize, objidl/IFillLockBytes::SetFillSize, stg.ifilllockbytes_setfillsize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFillLockBytes::SetFillSize
 - objidl/IFillLockBytes::SetFillSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IFillLockBytes.SetFillSize
---

# IFillLockBytes::SetFillSize


## -description

The 
<b>SetFillSize</b> method sets the expected size of the byte array.

## -parameters

### -param ulSize [in]

Size in bytes of the byte array object that is to be filled in subsequent calls to 
<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a>.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL.

## -remarks

If 
<b>SetFillSize</b> has not been called, any call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a> that attempts to access data that has not yet been written using 
<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a> or 
<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillat">IFillLockBytes::FillAt</a> will return a new error message, E_PENDING. After 
<b>SetFillSize</b> has been called, any call to 
<b>ReadAt</b> that attempts to access data beyond the current size, as set by 
<b>SetFillSize</b>, returns E_FAIL instead of E_PENDING.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillat">IFillLockBytes::FillAt</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a>