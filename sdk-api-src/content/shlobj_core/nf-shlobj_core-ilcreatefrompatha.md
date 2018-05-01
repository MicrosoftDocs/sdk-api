---
UID: NF:shlobj_core.ILCreateFromPathA
title: ILCreateFromPathA function
author: windows-driver-content
description: Returns the ITEMIDLIST structure associated with a specified file path.
old-location: shell\ILCreateFromPathW.htm
old-project: shell
ms.assetid: dee5486c-8be9-46c1-b5a1-e917e7c1e528
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ILCreateFromPath, ILCreateFromPath function [Windows Shell], ILCreateFromPathA, ILCreateFromPathW, _win32_ILCreateFromPathW, shell.ILCreateFromPathW, shlobj_core/ILCreateFromPath, shlobj_core/ILCreateFromPathA, shlobj_core/ILCreateFromPathW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h, Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ILCreateFromPathW (Unicode) and ILCreateFromPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	ILCreateFromPath
-	ILCreateFromPathA
-	ILCreateFromPathW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILCreateFromPathA function


## -description


Returns the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure associated with a specified file path.


## -parameters




### -param pszPath [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated Unicode string that contains the path. This string should be no more than MAX_PATH characters in length, including the terminating null character.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that corresponds to the path.




## -remarks



Call <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a> to release the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> when you are finished with it.



