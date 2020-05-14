---
UID: NS:richedit._clipboardformat
title: CLIPBOARDFORMAT (richedit.h)
description: Specifies the clipboard format. This structure included with the EN_CLIPFORMAT notification.helpviewer_keywords: ["CLIPBOARDFORMAT","CLIPBOARDFORMAT structure [Windows Controls]","controls.clipboardformat","richedit/CLIPBOARDFORMAT"]
old-location: controls\clipboardformat.htm
tech.root: Controls
ms.assetid: 5AD870B6-C4F1-446C-A516-171B24355EFA
ms.date: 12/05/2018
ms.keywords: CLIPBOARDFORMAT, CLIPBOARDFORMAT structure [Windows Controls], controls.clipboardformat, richedit/CLIPBOARDFORMAT
f1_keywords:
- richedit/CLIPBOARDFORMAT
dev_langs:
- c++
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- CLIPBOARDFORMAT
targetos: Windows
req.typenames: CLIPBOARDFORMAT
req.redist: 
ms.custom: 19H1
---

# CLIPBOARDFORMAT structure


## -description


Specifies the clipboard format. This structure included with the <a href="https://docs.microsoft.com/windows/desktop/Controls/en-clipformat">EN_CLIPFORMAT</a> notification. 



## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Structure that contains information about this notification message.


### -field cf

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A clipboard format registered by a call to the <a href="https://msdn.microsoft.com/892add91-a937-4602-86d2-5e5550a81872">RegisterClipboardFormat</a> function. 



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/en-clipformat">EN_CLIPFORMAT</a>
 

 

