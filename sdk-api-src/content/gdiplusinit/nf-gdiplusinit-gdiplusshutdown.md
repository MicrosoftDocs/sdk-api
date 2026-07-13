---
UID: NF:gdiplusinit.GdiplusShutdown
title: GdiplusShutdown function (gdiplusinit.h)
description: The GdiplusShutdown function cleans up resources used by Windows GDI+. Each call to GdiplusStartup should be paired with a call to GdiplusShutdown.
helpviewer_keywords: ["GdiplusShutdown","GdiplusShutdown function [GDI+]","_gdiplus_FUNC_GdiplusShutdown_","gdiplus._gdiplus_FUNC_GdiplusShutdown_","gdiplusinit/GdiplusShutdown"]
old-location: gdiplus\_gdiplus_FUNC_GdiplusShutdown_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\gdiplusshutdown.htm
ms.date: 12/05/2018
ms.keywords: GdiplusShutdown, GdiplusShutdown function [GDI+], _gdiplus_FUNC_GdiplusShutdown_, gdiplus._gdiplus_FUNC_GdiplusShutdown_, gdiplusinit/GdiplusShutdown
req.header: gdiplusinit.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GdiplusShutdown
 - gdiplusinit/GdiplusShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-gdi-gdiplus-l1-1-0.dll
 - Gdiplus.dll
api_name:
 - GdiplusShutdown
---

## -description

The <b>GdiplusShutdown</b> function cleans up resources used by Windows GDI+. Each call to <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> should be paired with a call to <b>GdiplusShutdown</b>.

## -parameters

### -param token

Type: [in] <b>ULONG_PTR</b>

Token returned by a previous call to <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>.

## -remarks

You must call <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> before you create any GDI+ objects, and you must delete all of your GDI+ objects (or have them go out of scope) before you call <b>GdiplusShutdown</b>.

<div class="alert"><b>Note</b>  For Windows 7 and earlier, if GDI+ can't create a font family, it substitutes the generic Sans Serif family and client-side caches the pointer for the generic family. Because calls to <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> and <b>GdiplusShutdown</b> are not aware of this caching, the operating system retains the pointer for the generic family object past the object's lifetime, which causes the operating system to crash. For Windows 8 and later, GDI+ returns a sentinel value for the generic family object that remains constant across calls to <b>GdiplusStartup</b> and <b>GdiplusShutdown</b> so the operating system doesn't retain the pointer for the generic family object past the object's lifetime.</div>
<div> </div>

#### Examples

For an example of calling <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> and <b>GdiplusShutdown</b>, see <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>.

## -see-also

<a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>

<a href="/windows/desktop/api/gdiplusinit/ns-gdiplusinit-gdiplusstartupinput">GdiplusStartupInput</a>

<a href="/windows/desktop/api/gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput">GdiplusStartupOutput</a>

<a href="/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting Started</a>