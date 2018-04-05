---
UID: NS:xapo.XAPO_PROCESS_BUFFER_PARAMETERS
title: XAPO_PROCESS_BUFFER_PARAMETERS
author: windows-driver-content
description: Defines stream buffer parameters that may change from one call to the next. Used with the Process method.
old-location: xaudio2\xapo_process_buffer_parameters.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapo.XAPO_PROCESS_BUFFER_PARAMETERS
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: XAPO_PROCESS_BUFFER_PARAMETERS, XAPO_PROCESS_BUFFER_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapo/XAPO_PROCESS_BUFFER_PARAMETERS, xaudio2.xapo_process_buffer_parameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: xapo.h
req.include-header: 
req.target-type: Windows
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
req.typenames: XAPO_PROCESS_BUFFER_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	xapo.h
api_name:
-	XAPO_PROCESS_BUFFER_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAPO_PROCESS_BUFFER_PARAMETERS structure


## -description


Defines stream buffer parameters that may change from one call to the next. Used with the <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a> method.


## -struct-fields




### -field pBuffer

Pointer to a stream buffer that contains audio data. The buffer must be 16-byte aligned, non-NULL, and must be at least <a href="https://msdn.microsoft.com/23090cfb-ab64-4399-9acb-f4c752a4be1b">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a>.MaxFrameCount frames in size. 



### -field BufferFlags

An <a href="https://msdn.microsoft.com/167d89bb-7cd3-4d1c-b233-c28a5cb2cef4">XAPO_BUFFER_FLAGS</a> enumeration describing the contents of the stream buffer.


### -field ValidFrameCount

Number of frames to process; this value must be within the range 0 to <a href="https://msdn.microsoft.com/23090cfb-ab64-4399-9acb-f4c752a4be1b">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a>.MaxFrameCount.


## -remarks



Although the format and maximum size values of a particular stream buffer are constant, as defined by the <a href="https://msdn.microsoft.com/23090cfb-ab64-4399-9acb-f4c752a4be1b">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structure, the actual memory address of the stream buffer is permitted to change. For constant-bit-rate (CBR) XAPOs, ValidFrameCount is constant and is always equal to the corresponding <b>XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</b>.MaxFrameCount for this buffer.

<div class="alert"><b>Note</b>  Only constant-bit-rate XAPOs are currently supported.</div>
<div> </div>


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

