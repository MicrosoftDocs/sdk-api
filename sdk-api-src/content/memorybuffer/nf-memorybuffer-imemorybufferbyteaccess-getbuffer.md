---
UID: NF:memorybuffer.IMemoryBufferByteAccess.GetBuffer
title: IMemoryBufferByteAccess::GetBuffer (memorybuffer.h)
description: Gets an IMemoryBuffer as an array of bytes.
helpviewer_keywords: ["GetBuffer","GetBuffer method [Windows Runtime]","GetBuffer method [Windows Runtime]","IMemoryBufferByteAccess interface","IMemoryBufferByteAccess interface [Windows Runtime]","GetBuffer method","IMemoryBufferByteAccess.GetBuffer","IMemoryBufferByteAccess::GetBuffer","memorybuffer/IMemoryBufferByteAccess::GetBuffer","winrt.imemorybufferbyteaccess_getbuffer"]
old-location: winrt\imemorybufferbyteaccess_getbuffer.htm
tech.root: WinRT
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [Windows Runtime], GetBuffer method [Windows Runtime],IMemoryBufferByteAccess interface, IMemoryBufferByteAccess interface [Windows Runtime],GetBuffer method, IMemoryBufferByteAccess.GetBuffer, IMemoryBufferByteAccess::GetBuffer, memorybuffer/IMemoryBufferByteAccess::GetBuffer, winrt.imemorybufferbyteaccess_getbuffer
req.header: memorybuffer.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMemoryBufferByteAccess::GetBuffer
 - memorybuffer/IMemoryBufferByteAccess::GetBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - memorybuffer.h
api_name:
 - IMemoryBufferByteAccess.GetBuffer
---

# IMemoryBufferByteAccess::GetBuffer


## -description

Gets an <a href="/uwp/api/windows.foundation.imemorybuffer">IMemoryBuffer</a> as an array of bytes.

## -parameters

### -param value [out]

A pointer to a byte array containing the buffer data.

### -param capacity [out]

The number of bytes in the returned array

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When <a href="/uwp/api/windows.foundation.memorybuffer.close">MemoryBuffer::Close</a> is called, the code using this buffer should set the <i>value</i> pointer to null.

## -see-also

<a href="/previous-versions/mt297505(v=vs.85)">IMemoryBufferByteAccess</a>