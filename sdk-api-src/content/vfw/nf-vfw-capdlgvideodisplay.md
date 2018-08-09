---
UID: NF:vfw.capDlgVideoDisplay
title: capDlgVideoDisplay macro
author: windows-sdk-content
description: The capDlgVideoDisplay macro displays a dialog box in which the user can set or adjust the video output.
old-location: multimedia\capdlgvideodisplay.htm
old-project: Multimedia
ms.assetid: 3feb6964-b897-4d5b-8861-7fca829e25e4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_capDlgVideoDisplay, capDlgVideoDisplay, capDlgVideoDisplay macro [Windows Multimedia], multimedia.capdlgvideodisplay, vfw/capDlgVideoDisplay"
ms.prod: windows
ms.technology: windows-sdk
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
 - capDlgVideoDisplay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capDlgVideoDisplay macro


## -description



The <b>capDlgVideoDisplay</b> macro displays a dialog box in which the user can set or adjust the video output. This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/151056f5-a9d1-4594-a8d7-32d4675ae3d6">WM_CAP_DLG_VIDEODISPLAY</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.

The Video Display dialog box is unique for each capture driver. Some capture drivers might not support a Video Display dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoDisplay</b> member of the <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

