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

# _MFCONTENTPROTECTIONDEVICE_OUTPUT_DATA structure


## -description


Contains information about the data you received as output from a protection system function.


## -struct-fields




### -field PrivateDataByteCount

The size of the private data that the implementation of the security processor reserves, in bytes. You can determine this value  by calling the <a href="https://msdn.microsoft.com/24FBA7E0-1496-4921-91C7-69E9AF830586">IMFContentProtectionDevice::GetPrivateDataByteCount</a> method.


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




<a href="https://msdn.microsoft.com/24FBA7E0-1496-4921-91C7-69E9AF830586">IMFContentProtectionDevice::GetPrivateDataByteCount</a>



<a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">IMFContentProtectionDevice::InvokeFunction</a>



<a href="https://msdn.microsoft.com/8D27592C-56EA-4E69-A1DC-2FAD56193CE2">MFCONTENTPROTECTIONDEVICE_INPUT_DATA</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

