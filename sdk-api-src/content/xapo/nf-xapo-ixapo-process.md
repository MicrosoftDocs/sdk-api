---
UID: NF:xapo.IXAPO.Process
title: IXAPO::Process (xapo.h)
description: Runs the XAPO's digital signal processing (DSP) code on the given input and output buffers.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","Process method","IXAPO.Process","IXAPO::Process","Process","Process method [XAudio2 Audio Mixing APIs]","Process method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::Process","xaudio2.ixapo_interface_process"]
old-location: xaudio2\ixapo_interface_process.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.Process(UINT32,const XAPO_PROCESS_BUFFER_PARAMETERS,UINT32,XAPO_PROCESS_BUFFER_PARAMETERS@,BOOL)
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],Process method, IXAPO.Process, IXAPO::Process, Process, Process method [XAudio2 Audio Mixing APIs], Process method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::Process, xaudio2.ixapo_interface_process
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPO::Process
 - xapo/IXAPO::Process
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.Process
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

Input array of <a href="/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters">XAPO_PROCESS_BUFFER_PARAMETERS</a> structures.

### -param OutputProcessParameterCount [in]

Number of elements in <i>pOutputProcessParameters</i>. 

<div class="alert"><b>Note</b>  XAudio2 currently supports only one input stream and one output stream.</div>
<div> </div>

### -param pOutputProcessParameters [in, out]

Output array of <a href="/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters">XAPO_PROCESS_BUFFER_PARAMETERS</a> structures. On input, the value of <b>XAPO_PROCESS_BUFFER_PARAMETERS</b>. <b>ValidFrameCount</b> indicates the number of frames that the XAPO should write to the output buffer. On output, the value of <b>XAPO_PROCESS_BUFFER_PARAMETERS</b>. <b>ValidFrameCount</b> indicates the actual number of frames written.

### -param IsEnabled

TRUE to process normally; FALSE to process thru. See Remarks for additional information.

## -remarks

Implementations of this function should not block, as the function is called from the realtime audio processing thread.



All code that could cause a delay, such as format validation and memory allocation, should be put in the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">IXAPO::LockForProcess</a> method, which is not called from the realtime audio processing thread. 



For in-place processing, the <i>pInputProcessParameters</i> parameter will not necessarily be the same as <i>pOutputProcessParameters</i>. Rather, their <i>pBuffer</i> members will point to the same memory. 



Multiple input and output buffers may be used with in-place XAPOs, though the input buffer count must equal the output buffer count. For in-place processing when multiple input and output buffers are used, the XAPO may assume the number of input buffers equals the number of output buffers. 



In addition to writing to the output buffer, as appropriate, an XAPO is responsible for setting the output stream's buffer flags and valid frame count. 



When <i>IsEnabled</i> is FALSE, the XAPO should not apply its normal processing to the given input/output buffers during. It should instead pass data from input to output with as little modification possible. Effects that perform format conversion should continue to do so. Effects must ensure transitions between normal and thru processing do not introduce discontinuities into the signal. 



When writing a <b>Process</b> method, it is important to note XAudio2 audio data is interleaved, which means data from each channel is adjacent for a particular sample number. For example, if there was a 4-channel wave playing into an XAudio2 source voice, the audio data would be a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>