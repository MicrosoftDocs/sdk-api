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

# _MTP_COMMAND_DATA_OUT structure


## -description



The <b>MTP_COMMAND_DATA_OUT</b> structure contains Media Transport Protocol (MTP) responses that are filled by the device driver on exiting a call to <a href="https://msdn.microsoft.com/3ef6a95d-d4e2-4608-9a02-98b497e1fdbb">IWMDMDevice3::DeviceIoControl</a>.




## -struct-fields




### -field ResponseCode

Response code.


### -field NumParams

Number of parameters for this response.


### -field Params

Parameters of the response. <b>MTP_RESPONSE_MAX_PARAMS</b> is a defined constant with a value of 5.


### -field CommandReadDataSize

Data size of <b>CommandReadData</b>[1], in bytes.


### -field CommandReadData

 




#### - CommandReadData[1]

Optional, first byte of data to read from the device if <b>MTP_COMMAND_DATA_IN.NextPhase</b> is MTP_NEXTPHASE_READ_DATA.


## -remarks



The input buffer is expected to contain an appropriately filled out <a href="https://msdn.microsoft.com/a7a6871b-3d53-4134-9877-398c532b489f">MTP_COMMAND_DATA_IN</a> structure. On exit, the device driver will fill out the <b>MTP_COMMAND_DATA_OUT</b> structure and save it to the output buffer. Therefore, any request must have an input buffer of at least SIZEOF_REQUIRED_COMMAND_DATA_IN bytes, which is defined as the following:

<pre class="syntax" xml:space="preserve"><code>
#define SIZEOF_REQUIRED_COMMAND_DATA_IN (sizeof(MTP_COMMAND_DATA_IN)-1)
</code></pre>
Any request must also have an output buffer of at least SIZEOF_REQUIRED_COMMAND_DATA_OUT bytes, which is defined as the following:

<pre class="syntax" xml:space="preserve"><code>
#define SIZEOF_REQUIRED_COMMAND_DATA_OUT (sizeof(MTP_COMMAND_DATA_OUT)-1)
</code></pre>
It is assumed that all commands are self-contained, that is, they can be processed completely in one call. This has implications on lengthy data transfers, because chunking in the traditional sense is not supported. (For example, to issue a read for 3megabytes, the caller would have to ensure that it allocates an output buffer of 3 MB plus <b>SIZEOF_REQUIRED_COMMAND_DATA_OUT</b> bytes.) Lengthy data transfers should not be done with this method, but rather through normal data transfer APIs.




## -see-also




<a href="https://msdn.microsoft.com/3ef6a95d-d4e2-4608-9a02-98b497e1fdbb">IWMDMDevice3::DeviceIoControl</a>



<a href="https://msdn.microsoft.com/a7a6871b-3d53-4134-9877-398c532b489f">MTP_COMMAND_DATA_IN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

