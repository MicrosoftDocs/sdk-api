---
UID: NS:winuser.tagMDICREATESTRUCTA
title: MDICREATESTRUCTA (winuser.h)
description: Contains information about the class, title, owner, location, and size of a multiple-document interface (MDI) child window. (ANSI)
helpviewer_keywords: ["*LPMDICREATESTRUCTA","LPMDICREATESTRUCT","LPMDICREATESTRUCT structure pointer [Windows and Messages]","MDICREATESTRUCT","MDICREATESTRUCT structure [Windows and Messages]","MDICREATESTRUCTA","MDICREATESTRUCTW","WS_HSCROLL","WS_MAXIMIZE","WS_MINIMIZE","WS_VSCROLL","_win32_MDICREATESTRUCT_str","_win32_mdicreatestruct_str_cpp","winmsg.mdicreatestruct","winui._win32_mdicreatestruct_str","winuser/LPMDICREATESTRUCT","winuser/MDICREATESTRUCT","winuser/MDICREATESTRUCTA","winuser/MDICREATESTRUCTW"]
old-location: winmsg\mdicreatestruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacestructures\mdicreatestruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPMDICREATESTRUCTA, LPMDICREATESTRUCT, LPMDICREATESTRUCT structure pointer [Windows and Messages], MDICREATESTRUCT, MDICREATESTRUCT structure [Windows and Messages], MDICREATESTRUCTA, MDICREATESTRUCTW, WS_HSCROLL, WS_MAXIMIZE, WS_MINIMIZE, WS_VSCROLL, _win32_MDICREATESTRUCT_str, _win32_mdicreatestruct_str_cpp, winmsg.mdicreatestruct, winui._win32_mdicreatestruct_str, winuser/LPMDICREATESTRUCT, winuser/MDICREATESTRUCT, winuser/MDICREATESTRUCTA, winuser/MDICREATESTRUCTW'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MDICREATESTRUCTW (Unicode) and MDICREATESTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MDICREATESTRUCTA, *LPMDICREATESTRUCTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMDICREATESTRUCTA
 - winuser/tagMDICREATESTRUCTA
 - LPMDICREATESTRUCTA
 - winuser/LPMDICREATESTRUCTA
 - MDICREATESTRUCTA
 - winuser/MDICREATESTRUCTA
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
 - MDICREATESTRUCT
 - MDICREATESTRUCTA
 - MDICREATESTRUCTW
---

# MDICREATESTRUCTA structure


## -description

Contains information about the class, title, owner, location, and size of a multiple-document interface (MDI) child window.

## -struct-fields

### -field szClass

Type: <b>LPCTSTR</b>

The name of the window class of the MDI child window. The class name must have been registered by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function.

### -field szTitle

Type: <b>LPCTSTR</b>

The title of the MDI child window. The system displays the title in the child window's title bar.

### -field hOwner

Type: <b>HANDLE</b>

A handle to the instance of the application creating the MDI client window.

### -field x

Type: <b>int</b>

The initial horizontal position, in client coordinates, of the MDI child window. If this member is <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default horizontal position.

### -field y

Type: <b>int</b>

The initial vertical position, in client coordinates, of the MDI child window. If this member is <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default vertical position.

### -field cx

Type: <b>int</b>

The initial width, in device units, of the MDI child window. If this member is <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default width.

### -field cy

Type: <b>int</b>

The initial height, in device units, of the MDI child window. If this member is set to <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default height.

### -field style

Type: <b>DWORD</b>


The style of the MDI child window. If the MDI client window was created with the <b>MDIS_ALLCHILDSTYLES</b> window style, this member can be any combination of the window styles listed in the <a href="/windows/desktop/winmsg/window-styles">Window Styles</a> page. Otherwise, this member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WS_MINIMIZE"></a><a id="ws_minimize"></a><dl>
<dt><b>WS_MINIMIZE</b></dt>
<dt>0x20000000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that is initially minimized.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_MAXIMIZE"></a><a id="ws_maximize"></a><dl>
<dt><b>WS_MAXIMIZE</b></dt>
<dt>0x01000000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that is initially maximized.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_HSCROLL"></a><a id="ws_hscroll"></a><dl>
<dt><b>WS_HSCROLL</b></dt>
<dt>0x00100000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that has a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_VSCROLL"></a><a id="ws_vscroll"></a><dl>
<dt><b>WS_VSCROLL</b></dt>
<dt>0x00200000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that has a vertical scroll bar.

</td>
</tr>
</table>

### -field lParam

Type: <b>LPARAM</b>

An application-defined value.

## -remarks

When the MDI client window creates an MDI child window
            by calling <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>, the system sends a <a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a> message to the created window. The <i>lParam</i> member of the <b>WM_CREATE</b> message contains a pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a> structure. The 
				<b>lpCreateParams</b> member of this structure contains a pointer to the <b>MDICREATESTRUCT</b> structure passed with the <a href="/windows/desktop/winmsg/wm-mdicreate">WM_MDICREATE</a> message that created the MDI child window.





> [!NOTE]
> The winuser.h header defines MDICREATESTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-clientcreatestruct">CLIENTCREATESTRUCT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/multiple-document-interface">Multiple Document Interface</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a>
