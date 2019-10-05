---
UID: NS:gdiplusinit.GdiplusStartupInput
title: GdiplusStartupInput (gdiplusinit.h)
author: windows-sdk-content
description: The GdiplusStartupInput structure holds a block of arguments that are required by the GdiplusStartup function.
old-location: gdiplus\_gdiplus_STRUC_GdiplusStartupInput.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusstartupinput.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GdiplusStartupInput, GdiplusStartupInput structure [GDI+], _gdiplus_STRUC_GdiplusStartupInput, gdiplus._gdiplus_STRUC_GdiplusStartupInput, gdiplusinit/GdiplusStartupInput
ms.topic: struct
f1_keywords: 
 - "gdiplusinit/GdiplusStartupInput"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusinit.h
api_name:
 - GdiplusStartupInput
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GdiplusStartupInput structure


## -description


The <b>GdiplusStartupInput</b> structure holds a block of arguments that are required by the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> function.


## -struct-fields




### -field GdiplusVersion

Type: <b>UINT32</b>

Specifies the version of GDI+. Must be 1. 


### -field DebugEventCallback

Type: <b>DebugEventProc</b>

Pointer to a callback function that GDI+ can call, on debug builds, for assertions and warnings. The default value is <b>NULL</b>. 


### -field SuppressBackgroundThread

Type: <b>BOOL</b>

Boolean value that specifies whether to suppress the GDI+ background thread. If you set this member to <b>TRUE</b>, <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a> returns (in its <i>output</i> parameter) a pointer to a hook function and a pointer to an unhook function. You must call those functions appropriately to replace the background thread. If you do not want to be responsible for calling the hook and unhook functions, set this member to <b>FALSE</b>. The default value is <b>FALSE</b>.


### -field SuppressExternalCodecs

Type: <b>BOOL</b>

Boolean value that specifies whether you want GDI+ to suppress external image codecs. GDI+ version 1.0 does not support external image codecs, so this parameter is ignored.


### -field GdiplusStartupInput

TBD 




## -remarks



The <b>GdiplusStartupInput</b> structure provides a constructor that sets the <b>GdiplusVersion</b> member to 1 and allows you to specify values for the other three members. All of the constructor parameters are optional, so you can declare a variable of type <b>GdiplusStartupInput</b> without passing any arguments to the constructor, and all of the members will be initialized with appropriate default values.

If you set the <b>SuppressBackgroundThread</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>Â <i>input</i> parameter to <b>TRUE</b>, you must call the hook and unhook functions returned in the <i>output</i> parameter. Call those functions before and after the application's main message loop; that is, a message loop that is active for the lifetime of GDI+. Call the hook function before the loop starts, and call the unhook function after the loop ends.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusshutdown">GdiplusShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/nf-gdiplusinit-gdiplusstartup">GdiplusStartup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput">GdiplusStartupOutput</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting Started</a>
 

 

