---
UID: NS:commctrl._TBBUTTON
title: TBBUTTON (commctrl.h)
description: Contains information about a button in a toolbar.
helpviewer_keywords: ["*LPTBBUTTON","*PTBBUTTON","LPTBBUTTON","LPTBBUTTON structure pointer [Windows Controls]","PTBBUTTON","PTBBUTTON structure pointer [Windows Controls]","TBBUTTON","TBBUTTON structure [Windows Controls]","_win32_TBBUTTON","_win32_TBBUTTON_cpp","commctrl/LPTBBUTTON","commctrl/PTBBUTTON","commctrl/TBBUTTON","controls.TBBUTTON","controls._win32_TBBUTTON"]
old-location: controls\TBBUTTON.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbbutton.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBBUTTON, *PTBBUTTON, LPTBBUTTON, LPTBBUTTON structure pointer [Windows Controls], PTBBUTTON, PTBBUTTON structure pointer [Windows Controls], TBBUTTON, TBBUTTON structure [Windows Controls], _win32_TBBUTTON, _win32_TBBUTTON_cpp, commctrl/LPTBBUTTON, commctrl/PTBBUTTON, commctrl/TBBUTTON, controls.TBBUTTON, controls._win32_TBBUTTON'
req.header: commctrl.h
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
targetos: Windows
req.typenames: TBBUTTON, *PTBBUTTON, *LPTBBUTTON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TBBUTTON
 - commctrl/_TBBUTTON
 - PTBBUTTON
 - commctrl/PTBBUTTON
 - TBBUTTON
 - commctrl/TBBUTTON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBBUTTON
---

## -description

Contains information about a button in a toolbar.

## -struct-fields

### -field iBitmap

Type: <b>int</b>

Zero-based index of the button image. Set this member to I_IMAGECALLBACK, and the toolbar will send the <a href="/windows/desktop/Controls/tbn-getdispinfo">TBN_GETDISPINFO</a> notification code to retrieve the image index when it is needed. 

<a href="/windows/desktop/Controls/common-control-versions">Version 5.81</a>. Set this member to I_IMAGENONE to indicate that the button does not have an image. The button layout will not include any space for a bitmap, only text.

If the button is a separator, that is, if <b>fsStyle</b> is set to <a href="/windows/desktop/Controls/toolbar-control-and-button-styles">BTNS_SEP</a>, <b>iBitmap</b> determines the width of the separator, in pixels. For information on selecting button images from image lists, see <a href="/windows/desktop/Controls/tb-setimagelist">TB_SETIMAGELIST</a> message.

### -field idCommand

Type: <b>int</b>

Command identifier associated with the button. This identifier is used in a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message when the button is chosen.

### -field fsState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Button state flags. This member can be a combination of the values listed in <a href="/windows/desktop/Controls/toolbar-button-states">Toolbar Button States</a>.

### -field fsStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Button style. This member can be a combination of the button style values listed in <a href="/windows/desktop/Controls/toolbar-control-and-button-styles">Toolbar Control and Button Styles</a>.

### -field bReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Reserved.

### -field dwData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

Application-defined value.

### -field iString

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT_PTR</a></b>

Zero-based index of the button string, or a pointer to a string buffer that contains text for the button.

## -remarks

The <b>iString</b> member can return either a string pointer or an index. You can use the <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a> macro to determine which is returned.