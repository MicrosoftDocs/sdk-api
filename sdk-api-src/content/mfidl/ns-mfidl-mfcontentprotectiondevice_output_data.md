---
UID: NS:mfidl._MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
title: MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA (mfidl.h)
description: Contains information about the data you received as output from a protection system function.
helpviewer_keywords: ["MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA","MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA structure [Media Foundation]","mf.mfcontentprotectiondevice_output_data","mfidl/MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA"]
old-location: mf\mfcontentprotectiondevice_output_data.htm
tech.root: mf
ms.assetid: 73380F30-E219-4670-86DA-63CDA10C94BF
ms.date: 12/05/2018
ms.keywords: MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA, MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA structure [Media Foundation], mf.mfcontentprotectiondevice_output_data, mfidl/MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
 - mfidl/_MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
 - MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
 - mfidl/MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA
---

# MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA structure


## -description

Contains information about the data you received as output from a protection system function.

## -struct-fields

### -field PrivateDataByteCount

The size of the private data that the implementation of the security processor reserves, in bytes. You can determine this value  by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-getprivatedatabytecount">IMFContentProtectionDevice::GetPrivateDataByteCount</a> method.

### -field MaxHWProtectionDataByteCount

The maximum size of data that the independent hardware vendor (IHV) can return in the output buffer, in bytes.

### -field HWProtectionDataByteCount

The size of the data that the  IHV wrote to the output buffer, in bytes.

### -field Status

The result of the protection system function.

### -field TransportTimeInHundredsOfNanoseconds

The number of 100 nanosecond units spent transporting the data.

### -field ExecutionTimeInHundredsOfNanoseconds

The number of 100 nanosecond units spent running the protection system function.

### -field OutputData

The output of the protection system function.

If the value of the <b>PrivateDataByteCount</b> member is greater than 0, bytes 0 through <b>PrivateDataByteCount</b> - 1 are reserved for IHV use.  
    Bytes <b>PrivateDataByteCount</b> through <b>MaxHWProtectionDataByteCount</b> + <b>PrivateDataByteCount</b> - 1 contain the region   
    of the array into which the driver should return the output data from the protection system function.

The protection system specification defines the format and size of the   
    function.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-getprivatedatabytecount">IMFContentProtectionDevice::GetPrivateDataByteCount</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">IMFContentProtectionDevice::InvokeFunction</a>



<a href="/windows/desktop/api/mfidl/ns-mfidl-mfcontentprotectiondevice_input_data">MFCONTENTPROTECTIONDEVICE_INPUT_DATA</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>