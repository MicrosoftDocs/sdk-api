---
UID: NF:vfw.capCaptureSequence
title: capCaptureSequence macro
author: windows-sdk-content
description: The capCaptureSequence macro initiates streaming video and audio capture to a file. You can use this macro or explicitly send the WM_CAP_SEQUENCE message.
old-location: multimedia\capcapturesequence.htm
tech.root: Multimedia
ms.assetid: cb4adf31-504a-46ee-b05e-768bdfde4b8f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "_win32_capCaptureSequence, capCaptureSequence, capCaptureSequence macro [Windows Multimedia], multimedia.capcapturesequence, vfw/capCaptureSequence"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Vfw.h
api_name:
 - capCaptureSequence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capCaptureSequence macro


## -description



The <b>capCaptureSequence</b> macro initiates streaming video and audio capture to a file. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/33d53abc-e37e-48c6-bfc8-9cd02fde5cb6">WM_CAP_SEQUENCE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



If you want to alter the parameters controlling streaming capture, use the <a href="https://msdn.microsoft.com/663dcb34-6b11-4208-b5d6-216799fb774d">capCaptureSetSetup</a> macro prior to starting the capture.

By default, the capture window does not allow other applications to continue running during capture. To override this, either set the <b>fYield</b> member of the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure to <b>TRUE</b>, or install a yield callback function.

During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions. To install callback procedures for these notifications, use the following macros:

<ul>
<li>
<a href="https://msdn.microsoft.com/1f9d3dba-be6d-4f7d-a80c-5bca8632e13f">capSetCallbackOnError</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7024aa3e-d227-4c22-8259-6299e9205f53">capSetCallbackOnStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c2e783a5-829b-4fa2-995a-c0cb4e63645b">capSetCallbackOnVideoStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/282386af-506b-4be6-bb75-aa3c62f9778a">capSetCallbackOnWaveStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/efddbcbc-f1e3-451c-928e-984eea187de2">capSetCallbackOnYield</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

