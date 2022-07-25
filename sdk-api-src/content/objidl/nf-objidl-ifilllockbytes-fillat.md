---
UID: NF:objidl.IFillLockBytes.FillAt
title: IFillLockBytes::FillAt (objidl.h)
description: The FillAt method writes a new block of data to a specified location in the byte array.
helpviewer_keywords: ["FillAt","FillAt method [Structured Storage]","FillAt method [Structured Storage]","IFillLockBytes interface","IFillLockBytes interface [Structured Storage]","FillAt method","IFillLockBytes.FillAt","IFillLockBytes::FillAt","_stg_ifilllockbytes_fillat","objidl/IFillLockBytes::FillAt","stg.ifilllockbytes_fillat"]
old-location: stg\ifilllockbytes_fillat.htm
tech.root: Stg
ms.assetid: d378d87b-e081-4950-b87b-9b1ad6dfb29d
ms.date: 12/05/2018
ms.keywords: FillAt, FillAt method [Structured Storage], FillAt method [Structured Storage],IFillLockBytes interface, IFillLockBytes interface [Structured Storage],FillAt method, IFillLockBytes.FillAt, IFillLockBytes::FillAt, _stg_ifilllockbytes_fillat, objidl/IFillLockBytes::FillAt, stg.ifilllockbytes_fillat
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
 - IFillLockBytes::FillAt
 - objidl/IFillLockBytes::FillAt
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
 - IFillLockBytes.FillAt
---

# IFillLockBytes::FillAt


## -description

The 
<b>FillAt</b> method writes a new block of data to a specified location in the byte array.

## -parameters

### -param ulOffset [in]

The offset, expressed in number of bytes, from the first element of the byte array.

### -param pv [in]

Pointer to the data to be written at the location specified by <i>uIOffset</i>.

### -param cb [in]

Size of <i>pv</i> in bytes.

### -param pcbWritten [out]

Number of bytes that were successfully written.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL in addition to the following:

| Return code | Description |
|----------------|---------------|
| E_NOTIMPL | The byte array does not support the **FillAt** method. |

## -remarks

The 
<b>FillAt</b> method is used for nonsequential downloading (for example, HTTP byte range requests). In nonsequential downloading the caller specifies ranges in the byte array where various blocks of data are to be written. Subsequent calls by the compound file implementation to <a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a> are passed by the byte array wrapper object's own implementation of 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> to the underlying byte array. This method is not currently implemented and will return E_NOTIMPL.

<div class="alert"><b>Note</b>  The system-supplied 
<a href="/windows/desktop/Stg/ifilllockbytes-implementation">IFillLockBytes</a> implementation does not support 
<b>FillAt</b> and returns E_NOTIMPL.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Stg/ifilllockbytes-implementation">IFillLockBytes - Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a>