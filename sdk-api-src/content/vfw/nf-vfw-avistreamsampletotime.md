---
UID: NF:vfw.AVIStreamSampleToTime
title: AVIStreamSampleToTime function
author: windows-sdk-content
description: The AVIStreamSampleToTime function converts a stream position from samples to milliseconds.
old-location: multimedia\avistreamsampletotime.htm
tech.root: Multimedia
ms.assetid: 376819cb-f803-4610-a9e8-29dc7059f203
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AVIStreamSampleToTime, AVIStreamSampleToTime function [Windows Multimedia], _win32_AVIStreamSampleToTime, multimedia.avistreamsampletotime, vfw/AVIStreamSampleToTime
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
api_name:
 - AVIStreamSampleToTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamSampleToTime function


## -description



The <b>AVIStreamSampleToTime</b> function converts a stream position from samples to milliseconds.




## -parameters




### -param pavi

Handle to an open stream.


### -param lSample

Position information. A sample can correspond to blocks of audio, a video frame, or other format, depending on the stream type.


## -returns



Returns the converted time if successful or â€“1 otherwise.




## -remarks



The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

