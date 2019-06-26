---
UID: NS:mfidl._MFCONTENTPROTECTIONDEVICE_INPUT_DATA
title: MFCONTENTPROTECTIONDEVICE_INPUT_DATA (mfidl.h)
author: windows-sdk-content
description: Contains information about the data that you want to provide as input to a protection system function.
old-location: mf\mfcontentprotectiondevice_input_data.htm
tech.root: medfound
ms.assetid: 8D27592C-56EA-4E69-A1DC-2FAD56193CE2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCONTENTPROTECTIONDEVICE_INPUT_DATA, MFCONTENTPROTECTIONDEVICE_INPUT_DATA structure [Media Foundation], mf.mfcontentprotectiondevice_input_data, mfidl/MFCONTENTPROTECTIONDEVICE_INPUT_DATA
ms.topic: struct
f1_keywords: 
 - "mfidl/MFCONTENTPROTECTIONDEVICE_INPUT_DATA"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCONTENTPROTECTIONDEVICE_INPUT_DATA
product: Windows
targetos: Windows
req.typenames: MFCONTENTPROTECTIONDEVICE_INPUT_DATA
req.redist: 
ms.custom: 19H1
---

# MFCONTENTPROTECTIONDEVICE_INPUT_DATA structure


## -description


Contains information about the data that you want to provide as input to a protection system function.


## -struct-fields




### -field HWProtectionFunctionID

The identifier of the function that you need to run. This value is defined by the implementation of the protection system.  


### -field PrivateDataByteCount

The size of the private data that the implementation of  the security processor implementation reserved. You can determine this value by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-getprivatedatabytecount">IMFContentProtectionDevice::GetPrivateDataByteCount</a> method.


### -field HWProtectionDataByteCount

The size of the data provided as input to the protection system function that you want to run.  


### -field Reserved

Reserved.


### -field InputData

The data to provide as input to the protection system function.

If the value of the <b>PrivateDataByteCount</b> member is greater than 0, bytes 0 through <b>PrivateDataByteCount</b> - 1 are reserved for use by the independent hardware vendor (IHV). Bytes <b>PrivateDataByteCount</b> through <b>HWProtectionDataByteCount</b> + <b>PrivateDataByteCount</b> - 1 contain the input data for the protection system function.   

The protection system specification defines the format and size of the DRM function.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-getprivatedatabytecount">IMFContentProtectionDevice::GetPrivateDataByteCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">IMFContentProtectionDevice::InvokeFunction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ns-mfidl-_mfcontentprotectiondevice_output_data">MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

