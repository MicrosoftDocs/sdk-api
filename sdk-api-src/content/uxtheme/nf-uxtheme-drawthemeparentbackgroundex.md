---
UID: NF:uxtheme.DrawThemeParentBackgroundEx
title: DrawThemeParentBackgroundEx function (uxtheme.h)
description: Used by partially-transparent or alpha-blended child controls to draw the part of their parent in front of which they appear. Sends a WM_ERASEBKGND message followed by a WM_PRINTCLIENT.
helpviewer_keywords: ["DTPB_USECTLCOLORSTATIC","DTPB_USEERASEBKGND","DTPB_WINDOWDC","DrawThemeParentBackgroundEx","DrawThemeParentBackgroundEx function [Windows Controls]","_shell_DrawThemeParentBackgroundEx","_shell_DrawThemeParentBackgroundEx_cpp","controls.DrawThemeParentBackgroundEx","controls._shell_DrawThemeParentBackgroundEx","uxtheme/DrawThemeParentBackgroundEx"]
old-location: controls\DrawThemeParentBackgroundEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeparentbackgroundex.htm
ms.date: 12/05/2018
ms.keywords: DTPB_USECTLCOLORSTATIC, DTPB_USEERASEBKGND, DTPB_WINDOWDC, DrawThemeParentBackgroundEx, DrawThemeParentBackgroundEx function [Windows Controls], _shell_DrawThemeParentBackgroundEx, _shell_DrawThemeParentBackgroundEx_cpp, controls.DrawThemeParentBackgroundEx, controls._shell_DrawThemeParentBackgroundEx, uxtheme/DrawThemeParentBackgroundEx
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawThemeParentBackgroundEx
 - uxtheme/DrawThemeParentBackgroundEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - DrawThemeParentBackgroundEx
---

# DrawThemeParentBackgroundEx function


## -description

Used by partially-transparent or alpha-blended child controls to draw the part of their parent in front of which they appear. Sends a <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message followed by a <a href="/windows/desktop/gdi/wm-printclient">WM_PRINTCLIENT</a>.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle of the child control.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC of the child control.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero or more of the following values. If this value is zero, this function returns S_OK only if the parent handled <a href="/windows/desktop/gdi/wm-printclient">WM_PRINTCLIENT</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTPB_WINDOWDC"></a><a id="dtpb_windowdc"></a><dl>
<dt><b>DTPB_WINDOWDC</b></dt>
</dl>
</td>
<td width="60%">
If set, <i>hdc</i> is assumed to be a window DC, not a client DC.

</td>
</tr>
<tr>
<td width="40%"><a id="DTPB_USECTLCOLORSTATIC"></a><a id="dtpb_usectlcolorstatic"></a><dl>
<dt><b>DTPB_USECTLCOLORSTATIC</b></dt>
</dl>
</td>
<td width="60%">
If set, this function sends a <a href="/windows/desktop/Controls/wm-ctlcolorstatic">WM_CTLCOLORSTATIC</a> message to the parent and uses the brush if one is provided. Otherwise, it uses COLOR_BTNFACE.

</td>
</tr>
<tr>
<td width="40%"><a id="DTPB_USEERASEBKGND"></a><a id="dtpb_useerasebkgnd"></a><dl>
<dt><b>DTPB_USEERASEBKGND</b></dt>
</dl>
</td>
<td width="60%">
If set, this function returns S_OK without sending a <a href="/windows/desktop/Controls/wm-ctlcolorstatic">WM_CTLCOLORSTATIC</a> message if the parent actually painted on <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a>.

</td>
</tr>
</table>

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Optional. The area to be drawn, in child coordinates. If this parameter is NULL, the area to be drawn includes the entire area occupied by the child control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

S_OK if successful; otherwise, S_FALSE.