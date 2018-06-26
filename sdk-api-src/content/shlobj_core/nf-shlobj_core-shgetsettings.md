---
UID: NF:shlobj_core.SHGetSettings
title: SHGetSettings function
author: windows-sdk-content
description: Retrieves the current Shell option settings.
old-location: shell\SHGetSettings.htm
old-project: shell
ms.assetid: 728a4004-f35d-4592-baf1-456a613a3344
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: SHGetSettings, SHGetSettings function [Windows Shell], SSF_DESKTOPHTML, SSF_DONTPRETTYPATH, SSF_DOUBLECLICKINWEBVIEW, SSF_HIDEICONS, SSF_MAPNETDRVBUTTON, SSF_NOCONFIRMRECYCLE, SSF_SHOWALLOBJECTS, SSF_SHOWATTRIBCOL, SSF_SHOWCOMPCOLOR, SSF_SHOWEXTENSIONS, SSF_SHOWINFOTIP, SSF_SHOWSYSFILES, SSF_WIN95CLASSIC, _win32_SHGetSettings, shell.SHGetSettings, shlobj_core/SHGetSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetSettings
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHGetSettings function


## -description


Retrieves the current Shell option settings.


## -parameters




### -param psfs

TBD


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


#### - lpsfs

Type: <b>LPSHELLFLAGSTATE</b>

The address of a <a href="https://msdn.microsoft.com/9968c7c9-79d9-4fb1-bda2-d6a2504cd3a3">SHELLFLAGSTATE</a> structure that receives the Shell option settings.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d7c2646c-03e0-4d7a-9503-bdf487d43723">SHGetSetSettings</a>
 

 

