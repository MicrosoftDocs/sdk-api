---
UID: NS:richedit._endropfiles
title: ENDROPFILES (richedit.h)
description: Contains information associated with an EN_DROPFILES notification code. A rich edit control sends this notification code when it receives a WM_DROPFILES message.
helpviewer_keywords: ["ENDROPFILES","ENDROPFILES structure [Windows Controls]","_win32_ENDROPFILES_str","_win32_ENDROPFILES_str_cpp","controls.ENDROPFILES","controls._win32_ENDROPFILES_str","richedit/ENDROPFILES"]
old-location: controls\ENDROPFILES.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\endropfiles.htm
ms.date: 12/05/2018
ms.keywords: ENDROPFILES, ENDROPFILES structure [Windows Controls], _win32_ENDROPFILES_str, _win32_ENDROPFILES_str_cpp, controls.ENDROPFILES, controls._win32_ENDROPFILES_str, richedit/ENDROPFILES
f1_keywords:
- richedit/ENDROPFILES
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
- ENDROPFILES
targetos: Windows
req.typenames: ENDROPFILES
req.redist: 
ms.custom: 19H1
---

# ENDROPFILES structure


## -description


Contains information associated with an <a href="https://msdn.microsoft.com/fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3">EN_DROPFILES</a> notification code. A rich edit control sends this notification code when it receives a <a href="https://docs.microsoft.com/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> message.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Notification header. 


### -field hDrop

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>

Handle to the dropped files list (same as with <a href="https://docs.microsoft.com/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> ). This handle is used with the <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-dragfinish">DragFinish</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-dragqueryfilea">DragQueryFile</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-dragquerypoint">DragQueryPoint</a> functions. 


### -field cp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Character position at which the dropped files would be inserted. 


### -field fProtected

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether the specified character position is protected (<b>TRUE</b>) or not protected (<b>FALSE</b>).

