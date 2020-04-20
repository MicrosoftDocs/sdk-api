---
UID: NS:richedit._ensaveclipboard
title: ENSAVECLIPBOARD (richedit.h)
description: Contains information about objects and text on the clipboard.helpviewer_keywords: ["ENSAVECLIPBOARD","ENSAVECLIPBOARD structure [Windows Controls]","_win32_ENSAVECLIPBOARD_str","_win32_ENSAVECLIPBOARD_str_cpp","controls.ENSAVECLIPBOARD","controls._win32_ENSAVECLIPBOARD_str","richedit/ENSAVECLIPBOARD"]
old-location: controls\ENSAVECLIPBOARD.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\ensaveclipboard.htm
ms.date: 12/05/2018
ms.keywords: ENSAVECLIPBOARD, ENSAVECLIPBOARD structure [Windows Controls], _win32_ENSAVECLIPBOARD_str, _win32_ENSAVECLIPBOARD_str_cpp, controls.ENSAVECLIPBOARD, controls._win32_ENSAVECLIPBOARD_str, richedit/ENSAVECLIPBOARD
f1_keywords:
- richedit/ENSAVECLIPBOARD
dev_langs:
- c++
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Richedit.h
api_name:
- ENSAVECLIPBOARD
targetos: Windows
req.typenames: ENSAVECLIPBOARD
req.redist: 
ms.custom: 19H1
---

# ENSAVECLIPBOARD structure


## -description


Contains information about objects and text on the clipboard.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> notification header. 


### -field cObjectCount

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Number of objects on the clipboard.


### -field cch

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Number of characters on the clipboard.


## -see-also




<a href="https://msdn.microsoft.com/e8b95e80-6494-4153-8e78-ede9ed17c66f">EN_SAVECLIPBOARD</a>
 

 

