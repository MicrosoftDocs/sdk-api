---
UID: NF:shobjidl.IStreamAsync.WriteAsync
title: IStreamAsync::WriteAsync (shobjidl.h)
description: Writes information to a stream asynchronously. For example, the Shell implements this method on file items when transferring them asynchronously.
helpviewer_keywords: ["IStreamAsync interface [Windows Shell]","WriteAsync method","IStreamAsync.WriteAsync","IStreamAsync::WriteAsync","WriteAsync","WriteAsync method [Windows Shell]","WriteAsync method [Windows Shell]","IStreamAsync interface","_shell_IStreamAsync_WriteAsync","shell.IStreamAsync_WriteAsync","shobjidl/IStreamAsync::WriteAsync"]
old-location: shell\IStreamAsync_WriteAsync.htm
tech.root: shell
ms.assetid: c5004923-191b-4ec1-83af-f066209c786a
ms.date: 12/05/2018
ms.keywords: IStreamAsync interface [Windows Shell],WriteAsync method, IStreamAsync.WriteAsync, IStreamAsync::WriteAsync, WriteAsync, WriteAsync method [Windows Shell], WriteAsync method [Windows Shell],IStreamAsync interface, _shell_IStreamAsync_WriteAsync, shell.IStreamAsync_WriteAsync, shobjidl/IStreamAsync::WriteAsync
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IStreamAsync::WriteAsync
 - shobjidl/IStreamAsync::WriteAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IStreamAsync.WriteAsync
---

# IStreamAsync::WriteAsync


## -description

Writes information to a stream asynchronously. For example, the Shell implements this method on file items when transferring them asynchronously.

## -parameters

### -param lpBuffer [in]

Type: <b>const void*</b>

A pointer to a buffer of size <i>cb</i> bytes that contains the information to be written to the stream.

### -param cb [in]

Type: <b>DWORD</b>

The size of the buffer pointed to by <i>lpBuffer</i>, in bytes.

### -param pcbWritten [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> value that, when the method returns successfully, states the actual number of bytes written to the stream. This value can be <b>NULL</b> if this information is not needed.

### -param lpOverlapped [in]

Type: <b>LPOVERLAPPED</b>

A pointer to an <a href="/windows/desktop/api/shobjidl/ns-shobjidl-overlapped">OVERLAPPED</a> structure that contains information used in the asynchronous write operation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>WriteAsync</b> should reset the event specified by the <b>hEvent</b> member of the <a href="/windows/desktop/api/shobjidl/ns-shobjidl-overlapped">OVERLAPPED</a> structure to a nonsignaled state when it begins the input/output (I/O) operation.