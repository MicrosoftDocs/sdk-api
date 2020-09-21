---
UID: NS:winuser.tagTPMPARAMS
title: TPMPARAMS (winuser.h)
description: Contains extended parameters for the TrackPopupMenuEx function.
helpviewer_keywords: ["*LPTPMPARAMS","LPTPMPARAMS","LPTPMPARAMS structure pointer [Menus and Other Resources]","TPMPARAMS","TPMPARAMS structure [Menus and Other Resources]","_win32_TPMPARAMS_str","_win32_tpmparams_str_cpp","menurc.tpmparams","winui._win32_tpmparams_str","winuser/LPTPMPARAMS","winuser/TPMPARAMS"]
old-location: menurc\tpmparams.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\tpmparams.htm
ms.date: 12/05/2018
ms.keywords: '*LPTPMPARAMS, LPTPMPARAMS, LPTPMPARAMS structure pointer [Menus and Other Resources], TPMPARAMS, TPMPARAMS structure [Menus and Other Resources], _win32_TPMPARAMS_str, _win32_tpmparams_str_cpp, menurc.tpmparams, winui._win32_tpmparams_str, winuser/LPTPMPARAMS, winuser/TPMPARAMS'
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: TPMPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTPMPARAMS
 - winuser/tagTPMPARAMS
 - TPMPARAMS
 - winuser/TPMPARAMS
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
 - TPMPARAMS
---

# TPMPARAMS structure


## -description

Contains extended parameters for the <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenuex">TrackPopupMenuEx</a> function.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size of structure, in bytes.

### -field rcExclude

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The rectangle to be excluded when positioning the window, in screen coordinates.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenuex">TrackPopupMenuEx</a>