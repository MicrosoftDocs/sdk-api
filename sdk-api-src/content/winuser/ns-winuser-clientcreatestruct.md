---
UID: NS:winuser.tagCLIENTCREATESTRUCT
title: CLIENTCREATESTRUCT (winuser.h)
description: Contains information about the menu and first multiple-document interface (MDI) child window of an MDI client window.
helpviewer_keywords: ["*LPCLIENTCREATESTRUCT","CLIENTCREATESTRUCT","CLIENTCREATESTRUCT structure [Windows and Messages]","LPCLIENTCREATESTRUCT","LPCLIENTCREATESTRUCT structure pointer [Windows and Messages]","_win32_CLIENTCREATESTRUCT_str","_win32_clientcreatestruct_str_cpp","winmsg.clientcreatestruct","winui._win32_clientcreatestruct_str","winuser/CLIENTCREATESTRUCT","winuser/LPCLIENTCREATESTRUCT"]
old-location: winmsg\clientcreatestruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\clientcreatestruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPCLIENTCREATESTRUCT, CLIENTCREATESTRUCT, CLIENTCREATESTRUCT structure [Windows and Messages], LPCLIENTCREATESTRUCT, LPCLIENTCREATESTRUCT structure pointer [Windows and Messages], _win32_CLIENTCREATESTRUCT_str, _win32_clientcreatestruct_str_cpp, winmsg.clientcreatestruct, winui._win32_clientcreatestruct_str, winuser/CLIENTCREATESTRUCT, winuser/LPCLIENTCREATESTRUCT'
req.header: winuser.h
req.include-header: Windows.h
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
targetos: Windows
req.typenames: CLIENTCREATESTRUCT, *LPCLIENTCREATESTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCLIENTCREATESTRUCT
 - winuser/tagCLIENTCREATESTRUCT
 - LPCLIENTCREATESTRUCT
 - winuser/LPCLIENTCREATESTRUCT
 - CLIENTCREATESTRUCT
 - winuser/CLIENTCREATESTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CLIENTCREATESTRUCT
---

# CLIENTCREATESTRUCT structure


## -description

Contains information about the menu and first multiple-document interface (MDI) child window of an MDI client window. An application passes a pointer to this structure as the
<i>lpParam</i> parameter of the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> function when creating an MDI client window.

## -struct-fields

### -field hWindowMenu

Type: <b>HANDLE</b>

A handle to the MDI application's window menu. An MDI application can retrieve this handle from the menu of the MDI frame window by using the <a href="/windows/desktop/api/winuser/nf-winuser-getsubmenu">GetSubMenu</a> function.

### -field idFirstChild

Type: <b>UINT</b>

The child window identifier of the first MDI child window created. The system increments the identifier for each additional MDI child window the application creates, and reassigns identifiers when the application destroys a window to keep the range of identifiers contiguous. These identifiers are used in <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages sent to the application's MDI frame window when a child window is chosen from the window menu; they should not conflict with any other command identifiers.

## -remarks

When the MDI client window is created by calling <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>, the system sends a <a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a> message to the window. The 
				<i>lParam</i> parameter of <b>WM_CREATE</b> contains a pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a> structure. The 
				<b>lpCreateParams</b> member of this structure contains a pointer to a <b>CLIENTCREATESTRUCT</b> structure.

## -see-also

<a href="/windows/desktop/winmsg/about-the-multiple-document-interface">About the Multiple Document Interface</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsubmenu">GetSubMenu</a>



<a href="/windows/desktop/api/winuser/ns-winuser-mdicreatestructa">MDICREATESTRUCT</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>