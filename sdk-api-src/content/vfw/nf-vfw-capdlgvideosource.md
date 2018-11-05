---
UID: NF:vfw.capDlgVideoSource
title: capDlgVideoSource macro
author: windows-sdk-content
description: The capDlgVideoSource macro displays a dialog box in which the user can control the video source.
old-location: multimedia\capdlgvideosource.htm
tech.root: Multimedia
ms.assetid: 9913a9e0-13ee-4f4b-9e8b-0f2549e4ded3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_capDlgVideoSource, capDlgVideoSource, capDlgVideoSource macro [Windows Multimedia], multimedia.capdlgvideosource, vfw/capDlgVideoSource"
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
 - capDlgVideoSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capDlgVideoSource macro


## -description



The <b>capDlgVideoSource</b> macro displays a dialog box in which the user can control the video source. The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8dc2f271-1f48-4e63-badf-9f3322063018">WM_CAP_DLG_VIDEOSOURCE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The Video Source dialog box is unique for each capture driver. Some capture drivers might not support a Video Source dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoSource</b> member of the <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

