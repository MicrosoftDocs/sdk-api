---
UID: NF:shlobj_core.ILCombine
title: ILCombine function
author: windows-driver-content
description: Combines two ITEMIDLIST structures.
old-location: shell\ILCombine.htm
old-project: shell
ms.assetid: 29eb1e1f-b7ac-4b72-8fce-a4388d7edfcc
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ILCombine, ILCombine function [Windows Shell], _win32_ILCombine, shell.ILCombine, shlobj_core/ILCombine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
-	Windows.Storage.dll
-	API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
-	ILCombine
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILCombine function


## -description


Combines two <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures.


## -parameters




### -param pidl1 [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the first <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


### -param pidl2 [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the second <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. This structure is appended to the structure pointed to by <i>pidl1</i>.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> containing the combined structures. If you set either <i>pidl1</i> or <i>pidl2</i> to <b>NULL</b>, the returned <b>ITEMIDLIST</b> structure is a clone of the non-<b>NULL</b> parameter. Returns <b>NULL</b> if <i>pidl1</i> and <i>pidl2</i> are both set to <b>NULL</b>.



