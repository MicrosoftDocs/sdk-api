---
UID: NS:gdiplusinit.GdiplusStartupOutput
title: GdiplusStartupOutput (gdiplusinit.h)
description: The GdiplusStartup function uses the GdiplusStartupOutput structure to return (in its output parameter) a pointer to a hook function and a pointer to an unhook function.
helpviewer_keywords: ["GdiplusStartupOutput","GdiplusStartupOutput structure [GDI+]","_gdiplus_STRUC_GdiplusStartupOutput","gdiplus._gdiplus_STRUC_GdiplusStartupOutput","gdiplusinit/GdiplusStartupOutput"]
old-location: gdiplus\_gdiplus_STRUC_GdiplusStartupOutput.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusstartupoutput.htm
ms.date: 12/05/2018
ms.keywords: GdiplusStartupOutput, GdiplusStartupOutput structure [GDI+], _gdiplus_STRUC_GdiplusStartupOutput, gdiplus._gdiplus_STRUC_GdiplusStartupOutput, gdiplusinit/GdiplusStartupOutput
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GdiplusStartupOutput
 - gdiplusinit/GdiplusStartupOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusinit.h
api_name:
 - GdiplusStartupOutput
---

## -description

The <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> function uses the <b>GdiplusStartupOutput</b> structure to return (in its <i>output</i> parameter) a pointer to a hook function and a pointer to an unhook function. If you set the <b>SuppressBackgroundThread</b> member of the <i>input</i> parameter to <b>TRUE</b>, then you are responsible for calling those functions to replace the Windows GDI+ background thread.

Call the hook and unhook functions before and after the application's main message loop; that is, a message loop that is active for the lifetime of GDI+. Call the hook function before the loop starts, and call the unhook function after the loop ends. The token parameter of the hook function receives an identifier that you should later pass to the unhook function. If you do not pass the proper identifier (the one returned by the hook function) to the unhook function, there will be resource leaks that won't be cleaned up until the process exits.

If you do not want to be responsible for calling the hook and unhook functions, set the <b>SuppressBackgroundThread</b> member of the <i>input</i> parameter (passed to <a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>) to <b>FALSE</b>.

## -struct-fields

### -field NotificationHook

Type: <b>NotificationHookProc</b>

Receives a pointer to a hook function.

### -field NotificationUnhook

Type: <b>NotificationUnhookProc</b>

Receives a pointer to an unhook function.

## -see-also

<a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusshutdown">GdiplusShutdown</a>

<a href="/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>

<a href="/windows/desktop/api/gdiplusinit/ns-gdiplusinit-gdiplusstartupinput">GdiplusStartupInput</a>

<a href="/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting started</a>