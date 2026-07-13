---
UID: NS:shlobj_core.SHELLSTATEA
title: SHELLSTATEA (shlobj_core.h)
description: Contains settings for the Shell's state. This structure is used with the SHGetSetSettings function. (ANSI)
helpviewer_keywords: ["*LPSHELLSTATEA","LPSHELLSTATE","LPSHELLSTATE structure pointer [Windows Shell]","SHELLSTATE","SHELLSTATE structure [Windows Shell]","SHELLSTATEA","SHELLSTATEW","_win32_SHELLSTATE","shell.SHELLSTATE","shlobj_core/LPSHELLSTATE","shlobj_core/SHELLSTATE"]
old-location: shell\SHELLSTATE.htm
tech.root: shell
ms.assetid: a5ba0e9f-d164-4fe6-97ab-34d61289ce1c
ms.date: 12/05/2018
ms.keywords: '*LPSHELLSTATEA, LPSHELLSTATE, LPSHELLSTATE structure pointer [Windows Shell], SHELLSTATE, SHELLSTATE structure [Windows Shell], SHELLSTATEA, SHELLSTATEW, _win32_SHELLSTATE, shell.SHELLSTATE, shlobj_core/LPSHELLSTATE, shlobj_core/SHELLSTATE'
req.header: shlobj_core.h
req.include-header: 
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
req.typenames: SHELLSTATEA, *LPSHELLSTATEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPSHELLSTATEA
 - shlobj_core/LPSHELLSTATEA
 - SHELLSTATEA
 - shlobj_core/SHELLSTATEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj_core.h
api_name:
 - SHELLSTATE
---

# SHELLSTATEA structure


## -description

Contains settings for the Shell's state. This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings">SHGetSetSettings</a> function.

## -struct-fields

### -field fShowAllObjects

Type: <b>BOOL</b>

<b>TRUE</b> to show all objects, including hidden files and folders. <b>FALSE</b> to hide hidden files and folders.

### -field fShowExtensions

Type: <b>BOOL</b>

<b>TRUE</b> to show file name extensions, <b>FALSE</b> to hide them.

### -field fNoConfirmRecycle

Type: <b>BOOL</b>

<b>TRUE</b> to show no confirmation dialog box when deleting items to the Recycle Bin, <b>FALSE</b> to display the confirmation dialog box.

### -field fShowSysFiles

Type: <b>BOOL</b>

<b>TRUE</b> to show system files, <b>FALSE</b> to hide them.

### -field fShowCompColor

Type: <b>BOOL</b>

<b>TRUE</b> to show encrypted or compressed NTFS files in color.

### -field fDoubleClickInWebView

Type: <b>BOOL</b>

<b>TRUE</b> to require a double-click to open an item when in web view.

### -field fDesktopHTML

Type: <b>BOOL</b>

<b>TRUE</b> to use Active Desktop, <b>FALSE</b> otherwise.

### -field fWin95Classic

Type: <b>BOOL</b>

<b>TRUE</b> to enforce Windows 95 Shell behavior and restrictions.

### -field fDontPrettyPath

Type: <b>BOOL</b>

<b>TRUE</b> to prevent the conversion of the path to all lowercase characters.

### -field fShowAttribCol

Type: <b>BOOL</b>

Not used.

### -field fMapNetDrvBtn

Type: <b>BOOL</b>

<b>TRUE</b> to display a <b>Map Network Drive</b> button.

### -field fShowInfoTip

Type: <b>BOOL</b>

<b>TRUE</b> to show a pop-up description for folders and files.

### -field fHideIcons

Type: <b>BOOL</b>

<b>TRUE</b> to hide desktop icons, <b>FALSE</b> to show them.

### -field fWebView

Type: <b>BOOL</b>

<b>TRUE</b> to display as a web view.

### -field fFilter

Type: <b>BOOL</b>

Not used.

### -field fShowSuperHidden

Type: <b>BOOL</b>

<b>TRUE</b> to show operating system files.

### -field fNoNetCrawling

Type: <b>BOOL</b>

<b>TRUE</b> to disable automatic searching for network folders and printers.

### -field dwWin95Unused

Type: <b>DWORD</b>

Not used.

### -field uWin95Unused

Type: <b>UINT</b>

Not used.

### -field lParamSort

Type: <b>LONG</b>

The column to sort by.

### -field iSortDirection

Type: <b>int</b>

Alphabetical sort direction for the column specified by <b>lParamSort</b>. Use 1 for an ascending sort, -1 for a descending sort.

### -field version

Type: <b>UINT</b>

Not used.

### -field uNotUsed

Type: <b>UINT</b>

Not used.

### -field fSepProcess

Type: <b>BOOL</b>

<b>TRUE</b> to launch folder windows in separate processes, <b>FALSE</b> to launch in the same process.

### -field fStartPanelOn

Type: <b>BOOL</b>

<b>Windows XP only</b>. <b>TRUE</b> to use the Windows XP-style Start menu, <b>FALSE</b> to use the classic Start menu.

### -field fShowStartPage

Type: <b>BOOL</b>

Not used.

### -field fAutoCheckSelect

Type: <b>BOOL</b>

<b>Introduced in Windows Vista</b>. <b>TRUE</b> to use the Windows Vista-style checkbox folder views, <b>FALSE</b> to use the classic views.

### -field fIconsOnly

Type: <b>BOOL</b>

<b>Introduced in Windows Vista</b>. <b>TRUE</b> to show generic icons only, <b>FALSE</b> to show thumbnail-style icons in folders.

### -field fShowTypeOverlay

Type: <b>BOOL</b>

<b>Introduced in Windows Vista</b>. <b>TRUE</b> indicates a thumbnail should show the application that would be invoked when opening the item, <b>FALSE</b> indicates that no application will be shown.

### -field fShowStatusBar

Type: <b>BOOL</b>

<b>Introduced in Windows 8</b>. <b>TRUE</b> to show the status bar; otherwise, <b>FALSE</b>.

### -field fSpareFlags

Type: <b>UINT</b>

Not used.

## -remarks

> [!NOTE]
> The shlobj_core.h header defines SHELLSTATE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

