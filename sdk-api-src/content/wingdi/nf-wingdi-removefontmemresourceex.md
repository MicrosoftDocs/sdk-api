---
UID: NF:wingdi.RemoveFontMemResourceEx
title: RemoveFontMemResourceEx function (wingdi.h)
description: The RemoveFontMemResourceEx function removes the fonts added from a memory image file.
helpviewer_keywords: ["RemoveFontMemResourceEx","RemoveFontMemResourceEx function [Windows GDI]","_win32_RemoveFontMemResourceEx","gdi.removefontmemresourceex","wingdi/RemoveFontMemResourceEx"]
old-location: gdi\removefontmemresourceex.htm
tech.root: gdi
ms.assetid: b73c3f1d-c508-418c-a5a2-105a35ec3a9b
ms.date: 12/05/2018
ms.keywords: RemoveFontMemResourceEx, RemoveFontMemResourceEx function [Windows GDI], _win32_RemoveFontMemResourceEx, gdi.removefontmemresourceex, wingdi/RemoveFontMemResourceEx
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemoveFontMemResourceEx
 - wingdi/RemoveFontMemResourceEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - RemoveFontMemResourceEx
---

# RemoveFontMemResourceEx function


## -description

The <b>RemoveFontMemResourceEx</b> function removes the fonts added from a memory image file.

## -parameters

### -param h [in]

A handle to the font-resource. This handle is returned by the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontmemresourceex">AddFontMemResourceEx</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. No extended error information is available.

## -remarks

This function removes a font that was added by the <a href="/windows/desktop/api/wingdi/nf-wingdi-addfontmemresourceex">AddFontMemResourceEx</a> function. To remove the font, specify the same path and flags as were used in <b>AddFontMemResourceEx</b>. This function will only remove the font that is specified by <i>fh</i>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontmemresourceex">AddFontMemResourceEx</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>