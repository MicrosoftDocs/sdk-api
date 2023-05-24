---
UID: NF:cfapi.CfSetPinState
title: CfSetPinState function (cfapi.h)
description: This sets the pin state of a placeholder, used to represent a user’s intent. Any application (not just the sync provider) can call this function.
helpviewer_keywords: ["CfSetPinState","CfSetPinState function","cfapi/CfSetPinState","cloudApi.cfsetpinstate"]
old-location: cloudapi\cfsetpinstate.htm
tech.root: cloudapi
ms.assetid: 8B279914-E23A-479B-8621-E83DE1978597
ms.date: 03/31/2023
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

This sets the pin state of a placeholder, used to represent a user’s intent. Any application (not just the sync provider) can call this function.

## -parameters

### -param FileHandle [in]

The handle of the placeholder file. The platform properly synchronizes the operation with other active requests. An attribute or no-access handle is sufficient. The caller must have **READ_DATA** or **WRITE_DAC** access to the placeholder, otherwise the operation will be failed with **STATUS_CLOUD_FILE_ACCESS_DENIED**.

### -param PinState [in]

The pin state of the placeholder file. For a list of valid *PinState* values, see [CF_PIN_STATE](ne-cfapi-cf_pin_state.md).

### -param PinFlags [in]

The pin state flags. *PinFlags* can be set to the following values:

- If **CF_PIN_FLAG_RECURSE** is specified, the platform applies the pin state to *FileHandle* and every file recursively beneath it (relevant only if *FileHandle* is a handle to a directory).
- If **CF_PIN_FLAG_RECURSE_ONLY** is specified, the platform applies the pin state to every file recursively beneath *FileHandle*, but not to *FileHandle* itself.
- If **CF_PIN_FLAG_RECURSE_STOP_ERROR** is specified, the platform will stop the recursion when encountering first error. Otherwise, the platform skips the error and continues the recursion.

### -param Overlapped [in, out, optional]

Allows the call to be performed asynchronously. See the [Remarks](#-remarks) section for more details.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

When specified and combined with an asynchronous *FileHandle*, *Overlapped* allows the platform to perform the call asynchronously.  

The caller must have initialized the overlapped structure with an event to wait on. If this returns **HRESULT_FROM_WIN32(ERROR_IO_PENDING)**, the caller can then wait using [GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.

## -see-also

[GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)

[CF_PIN_STATE](ne-cfapi-cf_pin_state.md)

[CF_SET_PIN_FLAGS](ne-cfapi-cf_set_pin_flags.md)
