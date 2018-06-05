---
UID: NS:gdiplusinit.GdiplusStartupOutput
title: GdiplusStartupOutput
author: windows-sdk-content
description: The GdiplusStartup function uses the GdiplusStartupOutput structure to return (in its output parameter) a pointer to a hook function and a pointer to an unhook function.
old-location: gdiplus\_gdiplus_STRUC_GdiplusStartupOutput.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusstartupoutput.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GdiplusStartupOutput, GdiplusStartupOutput structure [GDI+], _gdiplus_STRUC_GdiplusStartupOutput, gdiplus._gdiplus_STRUC_GdiplusStartupOutput, gdiplusinit/GdiplusStartupOutput
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusinit.h
api_name:
-	GdiplusStartupOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GdiplusStartupOutput structure


## -description


The <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> function uses the <b>GdiplusStartupOutput</b> structure to return (in its <i>output</i> parameter) a pointer to a hook function and a pointer to an unhook function. If you set the <b>SuppressBackgroundThread</b> member of the <i>input</i> parameter to <b>TRUE</b>, then you are responsible for calling those functions to replace the Windows GDI+ background thread.

Call the hook and unhook functions before and after the application's main message loop; that is, a message loop that is active for the lifetime of GDI+. Call the hook function before the loop starts, and call the unhook function after the loop ends. The token parameter of the hook function receives an identifier that you should later pass to the unhook function. If you do not pass the proper identifier (the one returned by the hook function) to the unhook function, there will be resource leaks that won't be cleaned up until the process exits.

If you do not want to be responsible for calling the hook and unhook functions, set the <b>SuppressBackgroundThread</b> member of the <i>input</i> parameter (passed to <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>) to <b>FALSE</b>.


## -struct-fields




### -field NotificationHook

Type: <b>NotificationHookProc</b>

Receives a pointer to a hook function. 


### -field NotificationUnhook

Type: <b>NotificationUnhookProc</b>

Receives a pointer to an unhook function. 


## -see-also




<a href="https://msdn.microsoft.com/88700669-cdfa-43dc-a5f1-a45db649b999">GdiplusShutdown</a>



<a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>



<a href="https://msdn.microsoft.com/dd0ffdd3-f05c-4ad4-a7c8-727d1d3ec83c">GdiplusStartupInput</a>



<a href="https://msdn.microsoft.com/c03c5ef1-13f6-4cf5-9395-be90b46aa6bb">Getting Started</a>
 

 

