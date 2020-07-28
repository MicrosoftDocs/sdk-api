---
UID: NF:vfw.ICGetState
title: ICGetState macro (vfw.h)
description: The ICGetState macro queries a video compression driver to return its current configuration in a block of memory. You can use this macro or explicitly call the ICM_GETSTATE message.
helpviewer_keywords: ["ICGetState","ICGetState macro [Windows Multimedia]","_win32_ICGetState","multimedia.icgetstate","vfw/ICGetState"]
old-location: multimedia\icgetstate.htm
tech.root: Multimedia
ms.assetid: e0066cc2-a67d-4cf4-9d22-506cc152ec14
ms.date: 12/05/2018
ms.keywords: ICGetState, ICGetState macro [Windows Multimedia], _win32_ICGetState, multimedia.icgetstate, vfw/ICGetState
f1_keywords:
- vfw/ICGetState
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
- ICGetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICGetState macro


## -description



The <b>ICGetState</b> macro queries a video compression driver to return its current configuration in a block of memory. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-getstate">ICM_GETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param pv

Pointer to a block of memory to contain the current configuration information. You can specify <b>NULL</b> for this parameter to determine the amount of memory required for the configuration information, as in <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icgetstatesize">ICGetStateSize</a>. 


### -param cb

Size, in bytes, of the block of memory. 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icgetstatesize">ICGetStateSize</a> macro returns the number of bytes used by the state data.

The structure used to represent configuration information is driver specific and is defined by the driver.

Use <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icgetstatesize">ICGetStateSize</a> before calling the <b>ICGetState</b> macro to determine the size of buffer to allocate for the call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

