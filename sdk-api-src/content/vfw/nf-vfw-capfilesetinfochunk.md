---
UID: NF:vfw.capFileSetInfoChunk
title: capFileSetInfoChunk macro (vfw.h)
description: The capFileSetInfoChunk macro sets and clears information chunks. Information chunks can be inserted in an AVI file during capture to embed text strings or custom data. You can use this macro or explicitly call the WM_CAP_FILE_SET_INFOCHUNK message.helpviewer_keywords: ["_win32_capFileSetInfoChunk","capFileSetInfoChunk","capFileSetInfoChunk macro [Windows Multimedia]","multimedia.capfilesetinfochunk","vfw/capFileSetInfoChunk"]
old-location: multimedia\capfilesetinfochunk.htm
tech.root: Multimedia
ms.assetid: b0772aa7-944c-450e-a703-0057a3230cb0
ms.date: 12/05/2018
ms.keywords: _win32_capFileSetInfoChunk, capFileSetInfoChunk, capFileSetInfoChunk macro [Windows Multimedia], multimedia.capfilesetinfochunk, vfw/capFileSetInfoChunk
f1_keywords:
- vfw/capFileSetInfoChunk
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
- capFileSetInfoChunk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capFileSetInfoChunk macro


## -description



The <b>capFileSetInfoChunk</b> macro sets and clears information chunks. Information chunks can be inserted in an AVI file during capture to embed text strings or custom data. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-file-set-infochunk">WM_CAP_FILE_SET_INFOCHUNK</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param lpInfoChunk

Pointer to a CAPINFOCHUNK structure defining the information chunk to be created or deleted. 


## -remarks



Multiple registered information chunks can be added to an AVI file. After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared. To clear a single entry, specify the information chunk in the <b>fccInfoID</b> member and <b>NULL</b> in the <b>lpData</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-capinfochunk">CAPINFOCHUNK</a> structure. To clear all entries, specify <b>NULL</b> in <b>fccInfoID</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

