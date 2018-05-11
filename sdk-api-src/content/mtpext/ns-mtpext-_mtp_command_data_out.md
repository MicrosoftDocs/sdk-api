---
UID: NS:mtpext._MTP_COMMAND_DATA_OUT
title: "_MTP_COMMAND_DATA_OUT"
author: windows-driver-content
description: The MTP_COMMAND_DATA_OUT structure contains Media Transport Protocol (MTP) responses that are filled by the device driver on exiting a call to IWMDMDevice3::DeviceIoControl.
old-location: wmdm\mtp_command_data_out.htm
old-project: WMDM
ms.assetid: ddaf49c8-99df-4e21-a633-82e08691f088
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PMTP_COMMAND_DATA_OUT, MTP_COMMAND_DATA_OUT, MTP_COMMAND_DATA_OUT structure [windows Media Device Manager], PMTP_COMMAND_DATA_OUT, PMTP_COMMAND_DATA_OUT structure pointer [windows Media Device Manager], _MTP_COMMAND_DATA_OUT, mtpext/MTP_COMMAND_DATA_OUT, mtpext/PMTP_COMMAND_DATA_OUT, wmdm.mtp_command_data_out"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mtpext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MTP_COMMAND_DATA_OUT, *PMTP_COMMAND_DATA_OUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MtpExt.h
api_name:
-	MTP_COMMAND_DATA_OUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

