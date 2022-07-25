---
UID: NF:mfidl.IMFContentProtectionDevice.GetPrivateDataByteCount
title: IMFContentProtectionDevice::GetPrivateDataByteCount (mfidl.h)
description: Gets the required number of bytes that need to be prepended to the input and output buffers when you call the security processor through the InvokeFunction method.
helpviewer_keywords: ["GetPrivateDataByteCount","GetPrivateDataByteCount method [Media Foundation]","GetPrivateDataByteCount method [Media Foundation]","IMFContentProtectionDevice interface","IMFContentProtectionDevice interface [Media Foundation]","GetPrivateDataByteCount method","IMFContentProtectionDevice.GetPrivateDataByteCount","IMFContentProtectionDevice::GetPrivateDataByteCount","mf.imfcontentprotectiondevice_getprivatedatabytecount","mfidl/IMFContentProtectionDevice::GetPrivateDataByteCount"]
old-location: mf\imfcontentprotectiondevice_getprivatedatabytecount.htm
tech.root: mf
ms.assetid: 24FBA7E0-1496-4921-91C7-69E9AF830586
ms.date: 12/05/2018
ms.keywords: GetPrivateDataByteCount, GetPrivateDataByteCount method [Media Foundation], GetPrivateDataByteCount method [Media Foundation],IMFContentProtectionDevice interface, IMFContentProtectionDevice interface [Media Foundation],GetPrivateDataByteCount method, IMFContentProtectionDevice.GetPrivateDataByteCount, IMFContentProtectionDevice::GetPrivateDataByteCount, mf.imfcontentprotectiondevice_getprivatedatabytecount, mfidl/IMFContentProtectionDevice::GetPrivateDataByteCount
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
 - IMFContentProtectionDevice::GetPrivateDataByteCount
 - mfidl/IMFContentProtectionDevice::GetPrivateDataByteCount
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
 - IMFContentProtectionDevice.GetPrivateDataByteCount
---

# IMFContentProtectionDevice::GetPrivateDataByteCount


## -description

     Gets the required number of bytes that need to be prepended to   
     the  input and output buffers when you call the security processor through the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">InvokeFunction</a> method.  
     When you specify this number of bytes, the Media Foundation transform (MFT) decryptor can allocate the total amount of bytes and can avoid making copies of the data when the decryptor moves the data to the security processor.

## -parameters

### -param PrivateInputByteCount [out]

The required number of bytes that need to be prepended to   
      the input buffer that you supply to content protection system.

### -param PrivateOutputByteCount [out]

The required number of bytes that need to be prepended to   
           the output buffer that you supply to content protection system.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">InvokeFunction</a>