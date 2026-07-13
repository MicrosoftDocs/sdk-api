---
UID: NF:cfapi.CfSetPinState
title: CfSetPinState function (cfapi.h)
description: This function sets the pin state of a placeholder, which represents a user’s intent. Any application, not just the sync provider, can call this function.
helpviewer_keywords: ["CfSetPinState","CfSetPinState function","cfapi/CfSetPinState","cloudApi.cfsetpinstate"]
old-location: cloudapi\cfsetpinstate.htm
tech.root: cloudapi
ms.assetid: 8B279914-E23A-479B-8621-E83DE1978597
ms.date: 11/13/2025
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

This function sets the pin state of a placeholder, which represents a user’s intent. Any application, not just the sync provider, can call this function.

## -parameters

### -param FileHandle [in]

The handle of the placeholder file. The platform properly synchronizes the operation with other active requests. An attribute or no-access handle is sufficient. The caller must have **READ_DATA** or **WRITE_DAC** access to the placeholder. Otherwise, the operation fails with **STATUS_CLOUD_FILE_ACCESS_DENIED**.

### -param PinState [in]

The pin state of the placeholder file. For a list of valid *PinState* values, see [CF_PIN_STATE](ne-cfapi-cf_pin_state.md).

### -param PinFlags [in]

The pin state flags. Set *PinFlags* to one of the following values:

- If you specify **CF_SET_PIN_FLAG_RECURSE**, the platform applies the pin state to *FileHandle* and every file recursively beneath it. This flag is relevant only if *FileHandle* is a handle to a directory.
- If you specify **CF_SET_PIN_FLAG_RECURSE_ONLY**, the platform applies the pin state to every file recursively beneath *FileHandle*, but not to *FileHandle* itself.
- If you specify **CF_SET_PIN_FLAG_RECURSE_STOP_ON_ERROR**, the platform stops the recursion when it encounters the first error. Otherwise, the platform skips the error and continues the recursion.

Use **CF_SET_PIN_FLAG_NONE** to specify no flags.

### -param Overlapped [in, out, optional]

Allows the call to be performed asynchronously. See the [Remarks](#-remarks) section for more details.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

When you specify and combine an asynchronous *FileHandle* with *Overlapped*, the platform can perform the call asynchronously.  

You must initialize the overlapped structure with an event to wait on. If this function returns **HRESULT_FROM_WIN32(ERROR_IO_PENDING)**, you can wait by using [GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). If you don't specify this parameter, the platform performs the API call synchronously, regardless of how you created the handle.

## -see-also

[GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)

[CF_PIN_STATE](ne-cfapi-cf_pin_state.md)

[CF_SET_PIN_FLAGS](ne-cfapi-cf_set_pin_flags.md)
