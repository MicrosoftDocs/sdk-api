---
UID: NF:shobjidl.IStreamAsync.OverlappedResult
title: IStreamAsync::OverlappedResult (shobjidl.h)

description: Retrieves the results of an overlapped operation.
old-location: shell\IStreamAsync_OverlappedResult.htm
tech.root: shell
ms.assetid: 5a53934f-bbff-4bb0-b374-01adb629a041

ms.date: 12/05/2018
ms.keywords: IStreamAsync interface [Windows Shell],OverlappedResult method, IStreamAsync.OverlappedResult, IStreamAsync::OverlappedResult, OverlappedResult, OverlappedResult method [Windows Shell], OverlappedResult method [Windows Shell],IStreamAsync interface, _shell_IStreamAsync_OverlappedResult, shell.IStreamAsync_OverlappedResult, shobjidl/IStreamAsync::OverlappedResult
ms.topic: method
f1_keywords:
- shobjidl/IStreamAsync.OverlappedResult
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- IStreamAsync.OverlappedResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamAsync::OverlappedResult


## -description


Retrieves the results of an overlapped operation.


## -parameters




### -param lpOverlapped [in]

Type: <b>LPOVERLAPPED*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ns-shobjidl-overlapped">OVERLAPPED</a> structure that was specified when the overlapped operation was started.


### -param lpNumberOfBytesTransferred [out]

Type: <b>LPDWORD</b>

When this method returns, contains the number of bytes that were actually transferred by a read or write operation.


### -param bWait [in]

Type: <b>BOOL</b>

If <b>TRUE</b> the method does not return until the operation has been completed.  If <b>FALSE</b> and an operation is pending, the method returns the HRESULT equivalent to ERROR_IO_INCOMPLETE.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



