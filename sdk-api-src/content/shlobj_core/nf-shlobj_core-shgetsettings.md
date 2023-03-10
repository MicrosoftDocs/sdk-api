---
UID: NF:shlobj_core.SHGetSettings
title: SHGetSettings function (shlobj_core.h)
description: Retrieves the current Shell option settings.
helpviewer_keywords: ["SHGetSettings","SHGetSettings function [Windows Shell]","SSF_DESKTOPHTML","SSF_DONTPRETTYPATH","SSF_DOUBLECLICKINWEBVIEW","SSF_HIDEICONS","SSF_MAPNETDRVBUTTON","SSF_NOCONFIRMRECYCLE","SSF_SHOWALLOBJECTS","SSF_SHOWATTRIBCOL","SSF_SHOWCOMPCOLOR","SSF_SHOWEXTENSIONS","SSF_SHOWINFOTIP","SSF_SHOWSYSFILES","SSF_WIN95CLASSIC","_win32_SHGetSettings","shell.SHGetSettings","shlobj_core/SHGetSettings"]
old-location: shell\SHGetSettings.htm
tech.root: shell
ms.assetid: 728a4004-f35d-4592-baf1-456a613a3344
ms.date: 12/05/2018
ms.keywords: SHGetSettings, SHGetSettings function [Windows Shell], SSF_DESKTOPHTML, SSF_DONTPRETTYPATH, SSF_DOUBLECLICKINWEBVIEW, SSF_HIDEICONS, SSF_MAPNETDRVBUTTON, SSF_NOCONFIRMRECYCLE, SSF_SHOWALLOBJECTS, SSF_SHOWATTRIBCOL, SSF_SHOWCOMPCOLOR, SSF_SHOWEXTENSIONS, SSF_SHOWINFOTIP, SSF_SHOWSYSFILES, SSF_WIN95CLASSIC, _win32_SHGetSettings, shell.SHGetSettings, shlobj_core/SHGetSettings
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetSettings
 - shlobj_core/SHGetSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetSettings
---

# SHGetSettings function


## -description

Retrieves the current Shell option settings.

## -parameters

### -param psfs

Type: <b>LPSHELLFLAGSTATE</b>

The address of a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate">SHELLFLAGSTATE</a> structure that receives the Shell option settings.

### -param dwMask

Type: <b>DWORD</b>

A set of flags that determine which members of <i>lpsfs</i> are being requested. This can be one or more of the following values.



#### SSF_DESKTOPHTML

The <b>fDesktopHTML</b> member is being requested.



#### SSF_DONTPRETTYPATH

The <b>fDontPrettyPath</b> member is being requested.



#### SSF_DOUBLECLICKINWEBVIEW

The <b>fDoubleClickInWebView</b> member is being requested.



#### SSF_HIDEICONS

The <b>fHideIcons</b> member is being requested.



#### SSF_MAPNETDRVBUTTON

The 
						<b>fMapNetDrvBtn</b> member is being requested.



#### SSF_NOCONFIRMRECYCLE

The 
						<b>fNoConfirmRecycle</b> member is being requested.



#### SSF_SHOWALLOBJECTS

The 
						<b>fShowAllObjects</b> member is being requested.



#### SSF_SHOWATTRIBCOL

The 
						<b>fShowAttribCol</b> member is being requested.



<b>Windows Vista:</b> Not used.





#### SSF_SHOWCOMPCOLOR

The 
						<b>fShowCompColor</b> member is being requested.



#### SSF_SHOWEXTENSIONS

The 
						<b>fShowExtensions</b> member is being requested.



#### SSF_SHOWINFOTIP

The 
						<b>fShowInfoTip</b> member is being requested.



#### SSF_SHOWSYSFILES

The 
						<b>fShowSysFiles</b> member is being requested.



#### SSF_WIN95CLASSIC

The 
						<b>fWin95Classic</b> member is being requested.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings">SHGetSetSettings</a>