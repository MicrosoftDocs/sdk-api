---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MFCONTENTPROTECTIONDEVICE_INPUT_DATA structure


## -description


Contains information about the data that you want to provide as input to a protection system function.


## -struct-fields




### -field HWProtectionFunctionID

The identifier of the function that you need to run. This value is defined by the implementation of the protection system.  


### -field PrivateDataByteCount

The size of the private data that the implementation of  the security processor implementation reserved. You can determine this value by calling the <a href="https://msdn.microsoft.com/24FBA7E0-1496-4921-91C7-69E9AF830586">IMFContentProtectionDevice::GetPrivateDataByteCount</a> method.


### -field HWProtectionDataByteCount

The size of the data provided as input to the protection system function that you want to run.  


### -field Reserved

Reserved.


### -field InputData

The data to provide as input to the protection system function.

If the value of the <b>PrivateDataByteCount</b> member is greater than 0, bytes 0 through <b>PrivateDataByteCount</b> - 1 are reserved for use by the independent hardware vendor (IHV). Bytes <b>PrivateDataByteCount</b> through <b>HWProtectionDataByteCount</b> + <b>PrivateDataByteCount</b> - 1 contain the input data for the protection system function.   

The protection system specification defines the format and size of the DRM function.


## -see-also




<a href="https://msdn.microsoft.com/24FBA7E0-1496-4921-91C7-69E9AF830586">IMFContentProtectionDevice::GetPrivateDataByteCount</a>



<a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">IMFContentProtectionDevice::InvokeFunction</a>



<a href="https://msdn.microsoft.com/73380F30-E219-4670-86DA-63CDA10C94BF">MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

