---
UID: NF:vfw.capFileSaveAs
title: capFileSaveAs macro (vfw.h)
description: The capFileSaveAs macro copies the contents of the capture file to another file. You can use this macro or explicitly call the WM_CAP_FILE_SAVEAS message.helpviewer_keywords: ["_win32_capFileSaveAs","capFileSaveAs","capFileSaveAs macro [Windows Multimedia]","multimedia.capfilesaveas","vfw/capFileSaveAs"]
old-location: multimedia\capfilesaveas.htm
tech.root: Multimedia
ms.assetid: 164bb345-c092-4adb-8f0f-83e31d36390f
ms.date: 12/05/2018
ms.keywords: _win32_capFileSaveAs, capFileSaveAs, capFileSaveAs macro [Windows Multimedia], multimedia.capfilesaveas, vfw/capFileSaveAs
f1_keywords:
- vfw/capFileSaveAs
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
- capFileSaveAs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capFileSaveAs macro


## -description



The <b>capFileSaveAs</b> macro copies the contents of the capture file to another file. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-file-saveas">WM_CAP_FILE_SAVEAS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to the null-terminated string that contains the name of the destination file used to copy the file. 


## -remarks



This message does not change the name or contents of the current capture file.

If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.

Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data. This message copies only the portion of the file containing the capture data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

