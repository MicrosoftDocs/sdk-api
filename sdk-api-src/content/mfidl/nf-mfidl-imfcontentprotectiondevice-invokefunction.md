---
UID: NF:mfidl.IMFContentProtectionDevice.InvokeFunction
title: IMFContentProtectionDevice::InvokeFunction (mfidl.h)
description: Calls into the implementation of the protection system in the security processor.
helpviewer_keywords: ["IMFContentProtectionDevice interface [Media Foundation]","InvokeFunction method","IMFContentProtectionDevice.InvokeFunction","IMFContentProtectionDevice::InvokeFunction","InvokeFunction","InvokeFunction method [Media Foundation]","InvokeFunction method [Media Foundation]","IMFContentProtectionDevice interface","mf.imfcontentprotectiondevice_invokefunction","mfidl/IMFContentProtectionDevice::InvokeFunction"]
old-location: mf\imfcontentprotectiondevice_invokefunction.htm
tech.root: mf
ms.assetid: 1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5
ms.date: 12/05/2018
ms.keywords: IMFContentProtectionDevice interface [Media Foundation],InvokeFunction method, IMFContentProtectionDevice.InvokeFunction, IMFContentProtectionDevice::InvokeFunction, InvokeFunction, InvokeFunction method [Media Foundation], InvokeFunction method [Media Foundation],IMFContentProtectionDevice interface, mf.imfcontentprotectiondevice_invokefunction, mfidl/IMFContentProtectionDevice::InvokeFunction
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentProtectionDevice::InvokeFunction
 - mfidl/IMFContentProtectionDevice::InvokeFunction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.dll
api_name:
 - IMFContentProtectionDevice.InvokeFunction
---

# IMFContentProtectionDevice::InvokeFunction


## -description

Calls into the implementation of the protection system in the security processor.

## -parameters

### -param FunctionId [in]

The identifier of the function that you want to run. This identifier is defined by the implementation of the protection system.

### -param InputBufferByteCount [in]

The number of bytes of in the buffer that <i>InputBuffer</i> specifies, including private data.

### -param InputBuffer [in]

A pointer to the data that you want to provide as input.

### -param OutputBufferByteCount [in, out]

Pointer to a value that specifies the length in bytes of the data that the function wrote to the buffer that <i>OutputBuffer</i> specifies, including the private data.

### -param OutputBuffer [out]

Pointer to the buffer where you want the function to write its output.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a>