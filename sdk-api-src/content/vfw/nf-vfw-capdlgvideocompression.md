---
UID: NF:vfw.capDlgVideoCompression
title: capDlgVideoCompression macro
author: windows-sdk-content
description: The capDlgVideoCompression macro displays a dialog box in which the user can select a compressor to use during the capture process.
old-location: multimedia\capdlgvideocompression.htm
old-project: Multimedia
ms.assetid: f4abf869-deac-4537-a8e8-680a4f138d0b
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "_win32_capDlgVideoCompression, capDlgVideoCompression, capDlgVideoCompression macro [Windows Multimedia], multimedia.capdlgvideocompression, vfw/capDlgVideoCompression"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capDlgVideoCompression
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capDlgVideoCompression macro


## -description



The <b>capDlgVideoCompression</b> macro displays a dialog box in which the user can select a compressor to use during the capture process. The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/526e4b5d-49a4-4bb5-92d6-cdd567636354">WM_CAP_DLG_VIDEOCOMPRESSION</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



Use this message with capture drivers that provide frames only in the BI_RGB format. This message is most useful in the step capture operation to combine capture and compression in a single operation. Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.

Compression does not affect the frames copied to the clipboard.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

