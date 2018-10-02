---
UID: NF:uxtheme.DrawThemeParentBackgroundEx
title: DrawThemeParentBackgroundEx function
author: windows-sdk-content
description: Used by partially-transparent or alpha-blended child controls to draw the part of their parent in front of which they appear. Sends a WM_ERASEBKGND message followed by a WM_PRINTCLIENT.
old-location: controls\DrawThemeParentBackgroundEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeparentbackgroundex.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: DTPB_USECTLCOLORSTATIC, DTPB_USEERASEBKGND, DTPB_WINDOWDC, DrawThemeParentBackgroundEx, DrawThemeParentBackgroundEx function [Windows Controls], _shell_DrawThemeParentBackgroundEx, _shell_DrawThemeParentBackgroundEx_cpp, controls.DrawThemeParentBackgroundEx, controls._shell_DrawThemeParentBackgroundEx, uxtheme/DrawThemeParentBackgroundEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - DrawThemeParentBackgroundEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawThemeParentBackgroundEx function


## -description


Used by partially-transparent or alpha-blended child controls to draw the part of their parent in front of which they appear. Sends a <a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a> message followed by a <a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a>.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the child control.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC of the child control.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero or more of the following values. If this value is zero, this function returns S_OK only if the parent handled <a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a>.

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
If set, this function sends a <a href="https://msdn.microsoft.com/en-us/library/Bb787524(v=VS.85).aspx">WM_CTLCOLORSTATIC</a> message to the parent and uses the brush if one is provided. Otherwise, it uses COLOR_BTNFACE.

</td>
</tr>
<tr>
<td width="40%"><a id="DTPB_USEERASEBKGND"></a><a id="dtpb_useerasebkgnd"></a><dl>
<dt><b>DTPB_USEERASEBKGND</b></dt>
</dl>
</td>
<td width="60%">
If set, this function returns S_OK without sending a <a href="https://msdn.microsoft.com/en-us/library/Bb787524(v=VS.85).aspx">WM_CTLCOLORSTATIC</a> message if the parent actually painted on <a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a>.

</td>
</tr>
</table>
 


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Optional. The area to be drawn, in child coordinates. If this parameter is NULL, the area to be drawn includes the entire area occupied by the child control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

S_OK if successful; otherwise, S_FALSE.



