---
UID: NF:wingdi.CreatePenIndirect
title: CreatePenIndirect function (wingdi.h)
description: The CreatePenIndirect function creates a logical cosmetic pen that has the style, width, and color specified in a structure.
helpviewer_keywords: ["CreatePenIndirect","CreatePenIndirect function [Windows GDI]","_win32_CreatePenIndirect","gdi.createpenindirect","wingdi/CreatePenIndirect"]
old-location: gdi\createpenindirect.htm
tech.root: gdi
ms.assetid: 638c0294-9a8f-44ed-a791-1be152cd92dd
ms.date: 12/05/2018
ms.keywords: CreatePenIndirect, CreatePenIndirect function [Windows GDI], _win32_CreatePenIndirect, gdi.createpenindirect, wingdi/CreatePenIndirect
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
 - CreatePenIndirect
 - wingdi/CreatePenIndirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreatePenIndirect
---

# CreatePenIndirect function


## -description

The <b>CreatePenIndirect</b> function creates a logical cosmetic pen that has the style, width, and color specified in a structure.

## -parameters

### -param plpen [in]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a> structure that specifies the pen's style, width, and color.

## -returns

If the function succeeds, the return value is a handle that identifies a logical cosmetic pen.

If the function fails, the return value is <b>NULL</b>.

## -remarks

After an application creates a logical pen, it can select that pen into a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

When you no longer need the pen, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a>



<a href="/windows/desktop/gdi/pen-functions">Pen Functions</a>



<a href="/windows/desktop/gdi/pens">Pens Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>