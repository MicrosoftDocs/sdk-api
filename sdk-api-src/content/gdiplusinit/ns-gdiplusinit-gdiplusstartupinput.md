---
UID: NS:gdiplusinit.GdiplusStartupInput
title: GdiplusStartupInput
author: windows-driver-content
description: The GdiplusStartupInput structure holds a block of arguments that are required by the GdiplusStartup function.
old-location: gdiplus\_gdiplus_STRUC_GdiplusStartupInput.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusstartupinput.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GdiplusStartupInput, GdiplusStartupInput structure [GDI+], _gdiplus_STRUC_GdiplusStartupInput, gdiplus._gdiplus_STRUC_GdiplusStartupInput, gdiplusinit/GdiplusStartupInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusinit.h
api_name:
-	GdiplusStartupInput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GdiplusStartupInput structure


## -description


The <b>GdiplusStartupInput</b> structure holds a block of arguments that are required by the <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> function.


## -struct-fields




### -field GdiplusVersion

Type: <b>UINT32</b>

Specifies the version of GDI+. Must be 1. 


### -field DebugEventCallback

Type: <b>DebugEventProc</b>

Pointer to a callback function that GDI+ can call, on debug builds, for assertions and warnings. The default value is <b>NULL</b>. 


### -field SuppressBackgroundThread

Type: <b>BOOL</b>

Boolean value that specifies whether to suppress the GDI+ background thread. If you set this member to <b>TRUE</b>, <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> returns (in its <i>output</i> parameter) a pointer to a hook function and a pointer to an unhook function. You must call those functions appropriately to replace the background thread. If you do not want to be responsible for calling the hook and unhook functions, set this member to <b>FALSE</b>. The default value is <b>FALSE</b>.


### -field SuppressExternalCodecs

Type: <b>BOOL</b>

Boolean value that specifies whether you want GDI+ to suppress external image codecs. GDI+ version 1.0 does not support external image codecs, so this parameter is ignored.


## -remarks



The <b>GdiplusStartupInput</b> structure provides a constructor that sets the <b>GdiplusVersion</b> member to 1 and allows you to specify values for the other three members. All of the constructor parameters are optional, so you can declare a variable of type <b>GdiplusStartupInput</b> without passing any arguments to the constructor, and all of the members will be initialized with appropriate default values.

If you set the <b>SuppressBackgroundThread</b> member of the <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>Â <i>input</i> parameter to <b>TRUE</b>, you must call the hook and unhook functions returned in the <i>output</i> parameter. Call those functions before and after the application's main message loop; that is, a message loop that is active for the lifetime of GDI+. Call the hook function before the loop starts, and call the unhook function after the loop ends.




## -see-also




<a href="https://msdn.microsoft.com/88700669-cdfa-43dc-a5f1-a45db649b999">GdiplusShutdown</a>



<a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>



<a href="https://msdn.microsoft.com/dcf89c6f-c0b2-4df0-910c-43d8d758fbaf">GdiplusStartupOutput</a>



<a href="https://msdn.microsoft.com/c03c5ef1-13f6-4cf5-9395-be90b46aa6bb">Getting Started</a>
 

 

