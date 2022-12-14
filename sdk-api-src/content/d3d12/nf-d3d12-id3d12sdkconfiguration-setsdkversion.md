---
UID: NF:d3d12.ID3D12SDKConfiguration.SetSDKVersion
title: ID3D12SDKConfiguration::SetSDKVersion
description: Configures the SDK version to use.
tech.root: direct3d12
ms.date: 08/25/2021
req.construct-type: function
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12SDKConfiguration::SetSDKVersion
 - d3d12/ID3D12SDKConfiguration::SetSDKVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12SDKConfiguration::SetSDKVersion
---

## -description

Configures the SDK version to use.

## -parameters

### -param SDKVersion

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The SDK version to set.

### -param SDKPath

Type: \_In\_z\_ **[LPCSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated string that provides the relative path to `d3d12core.dll` at the specified *SDKVersion*. The path is relative to the process exe of the caller. If `d3d12core.dll` isn't found, or isn't of the specified *SDKVersion*, then Direct3D 12 device creation fails.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, then it returns **S_OK**. Otherwise, it returns one of the [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues).

## -remarks

This method can be used only in Windows Developer Mode.

To set the SDK version using this API, you must call it before you create the Direct3D 12 device. Calling this API *after* creating the Direct3D 12 device will cause the Direct3D 12 runtime to remove the device.

If the `d3d12core.dll` installed with the OS is newer than the SDK version specified, then the OS version is used instead.

You can retrieve the version of a particular `D3D12Core.dll` from the exported symbol [**D3D12SDKVersion**](/windows/win32/direct3d12/nf-d3d12-d3d12sdkversion), which is a variable of type **UINT**, just like the variables exported from applications to enable use of the Agility SDK.

## -see-also
