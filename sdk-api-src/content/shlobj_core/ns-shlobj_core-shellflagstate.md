---
UID: NS:shlobj_core.SHELLFLAGSTATE
title: SHELLFLAGSTATE
author: windows-sdk-content
description: Contains a set of flags that indicate the current Shell settings. This structure is used with the SHGetSettings function.
old-location: shell\SHELLFLAGSTATE.htm
old-project: shell
ms.assetid: 9968c7c9-79d9-4fb1-bda2-d6a2504cd3a3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPSHELLFLAGSTATE, LPSHELLFLAGSTATE, LPSHELLFLAGSTATE structure pointer [Windows Shell], SHELLFLAGSTATE, SHELLFLAGSTATE structure [Windows Shell], _win32_SHELLFLAGSTATE, shell.SHELLFLAGSTATE, shlobj_core/LPSHELLFLAGSTATE, shlobj_core/SHELLFLAGSTATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: SHELLFLAGSTATE, *LPSHELLFLAGSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	SHELLFLAGSTATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# SHELLFLAGSTATE structure


## -description


Contains a set of flags that indicate the current Shell settings. This structure is used with the <a href="https://msdn.microsoft.com/728a4004-f35d-4592-baf1-456a613a3344">SHGetSettings</a> function.


## -struct-fields




### -field fShowAllObjects

Type: <b>BOOL</b>

Nonzero if the <b>Show All Files</b> option is enabled, or zero otherwise.


### -field fShowExtensions

Type: <b>BOOL</b>

Nonzero if the <b>Hide extensions for known file types</b> option is disabled, or zero otherwise.


### -field fNoConfirmRecycle

Type: <b>BOOL</b>

Nonzero if the <b>Display Delete Confirmation Dialog</b> box in the Recycle Bin is enabled, or zero otherwise.


### -field fShowSysFiles

Type: <b>BOOL</b>

Nonzero if the <b>Don't show hidden files, folders, or drives</b> option is selected, or zero otherwise.


### -field fShowCompColor

Type: <b>BOOL</b>

Nonzero if the <b>Display encrypted or compressed NTFS files in color</b> option is enabled, or zero otherwise.


### -field fDoubleClickInWebView

Type: <b>BOOL</b>

Nonzero if the <b>Double-Click to Open an Item</b> option is enabled, or zero otherwise.


### -field fDesktopHTML

Type: <b>BOOL</b>

Nonzero if the <b>Active Desktop – View as Web Page</b> option is enabled, or zero otherwise.


### -field fWin95Classic

Type: <b>BOOL</b>

Nonzero if the <b>Classic Style</b> option is enabled, or zero otherwise.


### -field fDontPrettyPath

Type: <b>BOOL</b>

Nonzero if the <b>Allow All Uppercase Names</b> option is enabled, or zero otherwise.


### -field fShowAttribCol

Type: <b>BOOL</b>

Nonzero if the <b>Show File Attributes in Detail View</b> option is enabled, or zero otherwise. 
                    

<b>Windows Vista and later</b>. Not used.


### -field fMapNetDrvBtn

Type: <b>BOOL</b>

Nonzero if the <b>Show Map Network Drive Button in Toolbar</b> option is enabled, or zero otherwise.


### -field fShowInfoTip

Type: <b>BOOL</b>

Nonzero if the <b>Show Info Tips for Items in Folders &amp; Desktop</b> option is enabled, or zero otherwise.


### -field fHideIcons

Type: <b>BOOL</b>

Nonzero if the <b>Show Desktop Icons</b> option is enabled, or zero otherwise.


### -field fAutoCheckSelect

Type: <b>BOOL</b>

<b>Windows Vista and later</b>: Nonzero if the <b>Use checkboxes to select  items</b> option is enabled, or zero otherwise.


### -field fIconsOnly

Type: <b>BOOL</b>

<b>Windows Vista and later</b>: Nonzero if the <b>Always show icons, never thumbnails</b> option is enabled, or zero otherwise.


### -field fRestFlags

Type: <b>UINT</b>

For Windows Vista this bitfield is 1, otherwise member this is not used.

