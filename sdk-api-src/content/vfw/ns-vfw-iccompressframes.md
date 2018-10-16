---
UID: NS:vfw.ICCOMPRESSFRAMES
title: ICCOMPRESSFRAMES
author: windows-sdk-content
description: The ICCOMPRESSFRAMES structure contains compression parameters used with the ICM_COMPRESS_FRAMES_INFO message.
old-location: multimedia\iccompressframes.htm
tech.root: Multimedia
ms.assetid: ced9ceea-d3fa-4496-886a-837545a28194
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ICCOMPRESSFRAMES, ICCOMPRESSFRAMES structure [Windows Multimedia], _win32_ICCOMPRESSFRAMES_str, multimedia.iccompressframes, vfw/ICCOMPRESSFRAMES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - ICCOMPRESSFRAMES
product: Windows
targetos: Windows
req.typenames: ICCOMPRESSFRAMES
req.redist: 
---

# ICCOMPRESSFRAMES structure


## -description



The <b>ICCOMPRESSFRAMES</b> structure contains compression parameters used with the <a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a> message.




## -struct-fields




### -field dwFlags

Applicable flags. The following value is defined: <b>ICCOMPRESSFRAMES_PADDING</b>. If this value is used, padding is used with the frame.
          


### -field lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format.
          


### -field lOutput

Reserved; do not use.
          


### -field lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input format.


### -field lInput

Reserved; do not use.


### -field lStartFrame

Number of the first frame to compress.


### -field lFrameCount

Number of frames to compress.


### -field lQuality

Quality setting.


### -field lDataRate

Maximum data rate, in bytes per second.


### -field lKeyRate

Maximum number of frames between consecutive key frames.


### -field dwRate

Compression rate in an integer format. To obtain the rate in frames per second, divide this value by the value in <b>dwScale</b>.


### -field dwScale

Value used to scale <b>dwRate</b> to frames per second.


### -field dwOverheadPerFrame

Reserved; do not use.


### -field dwReserved2

Reserved; do not use.


### -field GetData

Reserved; do not use.


### -field PutData

Reserved; do not use.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=16915">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a>



Video Compression Manager



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

