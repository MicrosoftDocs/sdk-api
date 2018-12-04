---
UID: NF:vfw.AVIStreamGetFrameOpen
title: AVIStreamGetFrameOpen function
author: windows-sdk-content
description: The AVIStreamGetFrameOpen function prepares to decompress video frames from the specified video stream.
old-location: multimedia\avistreamgetframeopen.htm
tech.root: Multimedia
ms.assetid: 467560b2-f79f-49ab-b019-d6315f0c2030
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: AVIStreamGetFrameOpen, AVIStreamGetFrameOpen function [Windows Multimedia], _win32_AVIStreamGetFrameOpen, multimedia.avistreamgetframeopen, vfw/AVIStreamGetFrameOpen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamGetFrameOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamGetFrameOpen function


## -description



The <b>AVIStreamGetFrameOpen</b> function prepares to decompress video frames from the specified video stream.




## -parameters




### -param pavi

Pointer to the video stream used as the video source.


### -param lpbiWanted

Pointer to a structure that defines the desired video format. Specify <b>NULL</b> to use a default format. You can also specify AVIGETFRAMEF_BESTDISPLAYFMT to decode the frames to the best format for your display.


## -returns



Returns a <b>GetFrame</b> object that can be used with the <a href="https://msdn.microsoft.com/9677efee-4c40-4acd-8911-eedcbee67d6b">AVIStreamGetFrame</a> function. If the system cannot find a decompressor that can decompress the stream to the given format, or to any RGB format, the function returns <b>NULL</b>.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

