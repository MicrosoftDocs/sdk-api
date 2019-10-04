---
UID: NF:vfw.capDlgVideoCompression
title: capDlgVideoCompression macro (vfw.h)
author: windows-sdk-content
description: The capDlgVideoCompression macro displays a dialog box in which the user can select a compressor to use during the capture process.
old-location: multimedia\capdlgvideocompression.htm
tech.root: Multimedia
ms.assetid: f4abf869-deac-4537-a8e8-680a4f138d0b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capDlgVideoCompression, capDlgVideoCompression, capDlgVideoCompression macro [Windows Multimedia], multimedia.capdlgvideocompression, vfw/capDlgVideoCompression"
ms.topic: macro
f1_keywords: 
 - "vfw/capDlgVideoCompression"
dev_langs:
 - c++
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
 - capDlgVideoCompression
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capDlgVideoCompression macro


## -description



The <b>capDlgVideoCompression</b> macro displays a dialog box in which the user can select a compressor to use during the capture process. The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-dlg-videocompression">WM_CAP_DLG_VIDEOCOMPRESSION</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



Use this message with capture drivers that provide frames only in the BI_RGB format. This message is most useful in the step capture operation to combine capture and compression in a single operation. Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.

Compression does not affect the frames copied to the clipboard.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

