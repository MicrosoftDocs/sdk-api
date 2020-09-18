---
UID: NF:vfw.DrawDibEnd
title: DrawDibEnd function (vfw.h)
description: The DrawDibEnd function clears the flags and other settings of a DrawDib DC that are set by the DrawDibBegin or DrawDibDraw functions.
helpviewer_keywords: ["DrawDibEnd","DrawDibEnd function [Windows Multimedia]","_win32_DrawDibEnd","multimedia.drawdibend","vfw/DrawDibEnd"]
old-location: multimedia\drawdibend.htm
tech.root: Multimedia
ms.assetid: 717f5404-b089-4556-8435-73ba5c52723a
ms.date: 12/05/2018
ms.keywords: DrawDibEnd, DrawDibEnd function [Windows Multimedia], _win32_DrawDibEnd, multimedia.drawdibend, vfw/DrawDibEnd
req.header: vfw.h
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibEnd
 - vfw/DrawDibEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibEnd
---

# DrawDibEnd function


## -description

The <b>DrawDibEnd</b> function clears the flags and other settings of a DrawDib DC that are set by the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibbegin">DrawDibBegin</a> or <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a> functions.

## -parameters

### -param hdd

Handle to the DrawDib DC to free.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>