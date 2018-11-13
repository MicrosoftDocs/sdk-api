---
UID: NF:vfw.AVIFileEndRecord
title: AVIFileEndRecord function
author: windows-sdk-content
description: The AVIFileEndRecord function marks the end of a record when writing an interleaved file that uses a 1:1 interleave factor of video to audio data. (Each frame of video is interspersed with an equivalent amount of audio data.).
old-location: multimedia\avifileendrecord.htm
tech.root: Multimedia
ms.assetid: 0f04c384-7702-43d4-9c7e-e9e74d6f2796
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AVIFileEndRecord, AVIFileEndRecord function [Windows Multimedia], _win32_AVIFileEndRecord, multimedia.avifileendrecord, vfw/AVIFileEndRecord
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
 - AVIFileEndRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIFileEndRecord function


## -description



The <b>AVIFileEndRecord</b> function marks the end of a record when writing an interleaved file that uses a 1:1 interleave factor of video to audio data. (Each frame of video is interspersed with an equivalent amount of audio data.)




## -parameters




### -param pfile

Handle to an open AVI file.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The <a href="https://msdn.microsoft.com/44200871-541c-4d67-ba12-61af06da8788">AVISave</a> function uses this function internally. In general, applications should not need to use this function.

The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

