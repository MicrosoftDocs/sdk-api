---
UID: NS:commctrl.tagCOLORSCHEME
title: COLORSCHEME (commctrl.h)
description: Contains information for the drawing of buttons in a toolbar or rebar.
helpviewer_keywords: ["*LPCOLORSCHEME","COLORSCHEME","COLORSCHEME structure [Windows Controls]","LPCOLORSCHEME","LPCOLORSCHEME structure pointer [Windows Controls]","_win32_COLORSCHEME","_win32_COLORSCHEME_cpp","commctrl/COLORSCHEME","commctrl/LPCOLORSCHEME","controls.COLORSCHEME","controls._win32_COLORSCHEME"]
old-location: controls\COLORSCHEME.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\colorscheme.htm
ms.date: 12/05/2018
ms.keywords: '*LPCOLORSCHEME, COLORSCHEME, COLORSCHEME structure [Windows Controls], LPCOLORSCHEME, LPCOLORSCHEME structure pointer [Windows Controls], _win32_COLORSCHEME, _win32_COLORSCHEME_cpp, commctrl/COLORSCHEME, commctrl/LPCOLORSCHEME, controls.COLORSCHEME, controls._win32_COLORSCHEME'
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
req.typenames: COLORSCHEME, *LPCOLORSCHEME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOLORSCHEME
 - commctrl/tagCOLORSCHEME
 - LPCOLORSCHEME
 - commctrl/LPCOLORSCHEME
 - COLORSCHEME
 - commctrl/COLORSCHEME
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
 - COLORSCHEME
---

# COLORSCHEME structure


## -description

Contains information for the drawing of buttons in a toolbar or rebar.

## -struct-fields

### -field dwSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size of this structure, in bytes.

### -field clrBtnHighlight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that represents the highlight color of the buttons. Use 
					<b>CLR_DEFAULT</b> for the default highlight color.

### -field clrBtnShadow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that represents the shadow color of the buttons. Use 
					<b>CLR_DEFAULT</b> for the default shadow color.