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

# IXAPO::Process


## -description


Runs the XAPO's digital signal processing (DSP) code on the given input and output buffers.


## -parameters




### -param InputProcessParameterCount [in]


Number of elements in pInputProcessParameters. 

<div class="alert"><b>Note</b>  XAudio2 currently supports only one input stream and one output stream.</div>
<div> </div>

### -param pInputProcessParameters [in]


Input array of <a href="https://msdn.microsoft.com/03f182f4-b051-4e2f-8b93-7e78dcf7e9ae">XAPO_PROCESS_BUFFER_PARAMETERS</a> structures. 


### -param OutputProcessParameterCount [in]

Number of elements in <i>pOutputProcessParameters</i>. 

<div class="alert"><b>Note</b>  XAudio2 currently supports only one input stream and one output stream.</div>
<div> </div>

### -param pOutputProcessParameters [in, out]

Output array of <a href="https://msdn.microsoft.com/03f182f4-b051-4e2f-8b93-7e78dcf7e9ae">XAPO_PROCESS_BUFFER_PARAMETERS</a> structures. On input, the value of <b>XAPO_PROCESS_BUFFER_PARAMETERS</b>. <b>ValidFrameCount</b> indicates the number of frames that the XAPO should write to the output buffer. On output, the value of <b>XAPO_PROCESS_BUFFER_PARAMETERS</b>. <b>ValidFrameCount</b> indicates the actual number of frames written.


### -param IsEnabled


TRUE to process normally; FALSE to process thru. See Remarks for additional information.


## -returns



This method does not return a value.




## -remarks



Implementations of this function should not block, as the function is called from the realtime audio processing thread.



All code that could cause a delay, such as format validation and memory allocation, should be put in the <a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">IXAPO::LockForProcess</a> method, which is not called from the realtime audio processing thread. 



For in-place processing, the <i>pInputProcessParameters</i> parameter will not necessarily be the same as <i>pOutputProcessParameters</i>. Rather, their <i>pBuffer</i> members will point to the same memory. 



Multiple input and output buffers may be used with in-place XAPOs, though the input buffer count must equal the output buffer count. For in-place processing when multiple input and output buffers are used, the XAPO may assume the number of input buffers equals the number of output buffers. 



In addition to writing to the output buffer, as appropriate, an XAPO is responsible for setting the output stream's buffer flags and valid frame count. 



When <i>IsEnabled</i> is FALSE, the XAPO should not apply its normal processing to the given input/output buffers during. It should instead pass data from input to output with as little modification possible. Effects that perform format conversion should continue to do so. Effects must ensure transitions between normal and thru processing do not introduce discontinuities into the signal. 



When writing a <b>Process</b> method, it is important to note XAudio2 audio data is interleaved, which means data from each channel is adjacent for a particular sample number. For example, if there was a 4-channel wave playing into an XAudio2 source voice, the audio data would be a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

