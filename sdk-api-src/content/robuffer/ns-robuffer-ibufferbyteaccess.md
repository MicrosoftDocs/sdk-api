---
UID: NS:robuffer.IBufferByteAccess
title: IBufferByteAccess
description: Represents a buffer as an array of bytes.
helpviewer_keywords: ["IBufferByteAccess interface [Windows Runtime]"]
old-location: winrt\ibufferbyteaccess_buffer.htm
tech.root: WinRT
ms.assetid: 51E69696-CE8A-4390-8134-EE5C5F3C729B
ms.date: 12/5/2018
ms.keywords: IBufferByteAccess interface [Windows Runtime]
req.header: robuffer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
f1_keywords:
 - IBufferByteAccess
 - robuffer/IBufferByteAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - robuffer.h
api_name:
 - IBufferByteAccess
---

## -description

Represents a buffer as an array of bytes.

## -struct-fields

### -field IUnknown

## -remarks

The client creates an [IBuffer](/uwp/api/Windows.Storage.Streams.IBuffer) object, and the buffer is provided by the [Buffer](nf-robuffer-ibufferbyteaccess-buffer.md) method.

When you implement the **IBuffer** interface, you must implement the **IBufferByteAccess** interface.

## -see-also