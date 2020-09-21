---
UID: NF:magnification.MagSetWindowFilterList
title: MagSetWindowFilterList function (magnification.h)
description: Sets the list of windows to be magnified or the list of windows to be excluded from magnification.
helpviewer_keywords: ["MagSetWindowFilterList","MagSetWindowFilterList function [Magnification API]","magapi.magapi_MagSetWindowFilterList","magapi_MagSetWindowFilterList","magnification/MagSetWindowFilterList"]
old-location: magapi\magapi_MagSetWindowFilterList.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetwindowfilterlist.htm
ms.date: 12/05/2018
ms.keywords: MagSetWindowFilterList, MagSetWindowFilterList function [Magnification API], magapi.magapi_MagSetWindowFilterList, magapi_MagSetWindowFilterList, magnification/MagSetWindowFilterList
req.header: magnification.h
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
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MagSetWindowFilterList
 - magnification/MagSetWindowFilterList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagSetWindowFilterList
---

# MagSetWindowFilterList function


## -description

Sets the list of windows to be magnified or the 
		list of windows to be excluded from magnification.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the magnification window.

### -param dwFilterMode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The magnification filter mode. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MW_FILTERMODE_INCLUDE</td>
<td>Magnify the windows.
<div class="alert"><b>Note:</b>  This value is not supported on Windows 7 or newer.</div>
<div> </div>


</td>
</tr>
<tr>
<td>MW_FILTERMODE_EXCLUDE</td>
<td>Exclude the windows from magnification.</td>
</tr>
</table>

### -param count [in]

Type: <b>int</b>

The number of window handles in the list.

### -param pHWND [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a>*</b>

The list of window handles.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

This function requires Windows Display Driver Model (WDDM)-capable video cards.

Only one window list is used. You can specify either MW_FILTERMODE_INCLUDE or MW_FILTERMODE_EXCLUDE, 
		depending on whether it is more convenient to list included windows or excluded windows.

The magnification window itself is automatically excluded.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetwindowfilterlist">MagGetWindowFilterList</a>