---
UID: NF:vfw.ICGetDefaultQuality
title: ICGetDefaultQuality macro (vfw.h)
description: The ICGetDefaultQuality macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the ICM_GETDEFAULTQUALITY message.
helpviewer_keywords: ["ICGetDefaultQuality","ICGetDefaultQuality macro [Windows Multimedia]","_win32_ICGetDefaultQuality","multimedia.icgetdefaultquality","vfw/ICGetDefaultQuality"]
old-location: multimedia\icgetdefaultquality.htm
tech.root: Multimedia
ms.assetid: dd88a141-5461-4725-83f9-c2ead3a3a2b6
ms.date: 12/05/2018
ms.keywords: ICGetDefaultQuality, ICGetDefaultQuality macro [Windows Multimedia], _win32_ICGetDefaultQuality, multimedia.icgetdefaultquality, vfw/ICGetDefaultQuality
f1_keywords:
- vfw/ICGetDefaultQuality
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
- ICGetDefaultQuality
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICGetDefaultQuality macro


## -description



The <b>ICGetDefaultQuality</b> macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-getdefaultquality">ICM_GETDEFAULTQUALITY</a> message.




## -parameters




### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the default quality value. Quality values range from 0 to 10,000. 


## -remarks



The <b>ICGetDefaultQuality</b> macro returns the default quality value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

