---
UID: NF:cfapi.CfSetPinState
title: CfSetPinState function (cfapi.h)
description: This sets the pin state of a placeholder, used to represent a user’s intent. Any application (not just the sync provider) can call this function.
helpviewer_keywords: ["CfSetPinState","CfSetPinState function","cfapi/CfSetPinState","cloudApi.cfsetpinstate"]
old-location: cloudapi\cfsetpinstate.htm
tech.root: cloudapi
ms.assetid: 8B279914-E23A-479B-8621-E83DE1978597
ms.date: 12/05/2018
ms.keywords: CfSetPinState, CfSetPinState function, cfapi/CfSetPinState, cloudApi.cfsetpinstate
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfSetPinState
 - cfapi/CfSetPinState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfSetPinState
---

# CfSetPinState function


## -description

This sets the pin state of a placeholder, used to represent a user’s intent.  Any application (not just the sync provider) can call this function.

## -parameters

### -param FileHandle [in]

The handle of the placeholder file. The caller must have READ_DATA or WRITE_DAC access to the placeholder.

### -param PinState [in]

The pin state of the placeholder file.

### -param PinFlags [in]

The pin state flags.

### -param Overlapped [in, out, optional]

Allows the call to be performed asynchronously. See the Remarks section for more details.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When specified and combined with an asynchronous <i>FileHandle</i>, <i>Overlapped</i> allows the platform to perform the call asynchronously.  

The caller must have initialized the overlapped structure with an event to wait on. If this returns HRESULT_FROM_WIN32(ERROR_IO_PENDING), the caller can then wait using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>. If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.