---
UID: NF:vfw.capDlgVideoFormat
title: capDlgVideoFormat macro (vfw.h)
description: The capDlgVideoFormat macro displays a dialog box in which the user can select the video format.helpviewer_keywords: ["_win32_capDlgVideoFormat","capDlgVideoFormat","capDlgVideoFormat macro [Windows Multimedia]","multimedia.capdlgvideoformat","vfw/capDlgVideoFormat"]
old-location: multimedia\capdlgvideoformat.htm
tech.root: Multimedia
ms.assetid: 542913e8-c3f4-4ea5-afa0-035af6f3126e
ms.date: 12/05/2018
ms.keywords: _win32_capDlgVideoFormat, capDlgVideoFormat, capDlgVideoFormat macro [Windows Multimedia], multimedia.capdlgvideoformat, vfw/capDlgVideoFormat
f1_keywords:
- vfw/capDlgVideoFormat
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
- capDlgVideoFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capDlgVideoFormat macro


## -description



The <b>capDlgVideoFormat</b> macro displays a dialog box in which the user can select the video format. The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-dlg-videoformat">WM_CAP_DLG_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



After this message returns, applications might need to update the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-capstatus">CAPSTATUS</a> structure because the user might have changed the image dimensions.

The Video Format dialog box is unique for each capture driver. Some capture drivers might not support a Video Format dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoFormat</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-capdrivercaps">CAPDRIVERCAPS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

