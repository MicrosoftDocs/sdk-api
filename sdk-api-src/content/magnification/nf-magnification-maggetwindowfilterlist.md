---
UID: NF:magnification.MagGetWindowFilterList
title: MagGetWindowFilterList function (magnification.h)
description: Retrieves the list of windows that are magnified or excluded from magnification.
helpviewer_keywords: ["MagGetWindowFilterList","MagGetWindowFilterList function [Magnification API]","magapi.magapi_MagGetWindowFilterList","magapi_MagGetWindowFilterList","magnification/MagGetWindowFilterList"]
old-location: magapi\magapi_MagGetWindowFilterList.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowfilterlist.htm
ms.date: 12/05/2018
ms.keywords: MagGetWindowFilterList, MagGetWindowFilterList function [Magnification API], magapi.magapi_MagGetWindowFilterList, magapi_MagGetWindowFilterList, magnification/MagGetWindowFilterList
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
 - MagGetWindowFilterList
 - magnification/MagGetWindowFilterList
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
 - MagGetWindowFilterList
---

# MagGetWindowFilterList function


## -description

Retrieves the list of windows that are magnified or excluded from magnification.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

### -param pdwFilterMode [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The filter mode, as set by <a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetwindowfilterlist">MagSetWindowFilterList</a>.

### -param count [in]

Type: <b>int</b>

The number of windows to retrieve, or 0 to retrieve a count of windows in the filter list.

### -param pHWND [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a>*</b>

The list of window handles.

## -returns

Type: <b>int</b>

Returns the count of window handles in the filter list, or -1 if the <i>hwnd</i> parameter is not valid.

## -remarks

First call the method with a <i>count</i> of 0 to retrieve the count of windows in the filter list. Use the retrieved count to allocate
			sufficient memory for the retrieved list of window handles.

This function requires Windows Display Driver Model (WDDM)-capable video cards.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetwindowfilterlist">MagSetWindowFilterList</a>