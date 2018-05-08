---
UID: NF:shlobj_core.ILFindLastID
title: ILFindLastID function
author: windows-driver-content
description: Returns a pointer to the last SHITEMID structure in an ITEMIDLIST structure.
old-location: shell\ILFindLastID.htm
old-project: shell
ms.assetid: 877029b7-a2fb-42c2-98a1-0eb6f229f1d9
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ILFindLastID, ILFindLastID function [Windows Shell], _win32_ILFindLastID, shell.ILFindLastID, shlobj_core/ILFindLastID
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
-	Ext-MS-Win-shell-shell32-l1-2-0.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
-	API-MS-Win-Shell-Namespace-L1-1-0.dll
-	Windows.Storage.dll
api_name:
-	ILFindLastID
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILFindLastID function


## -description


Returns a pointer to the last <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -returns



Type: <b>PUITEMID_CHILD</b>

A pointer to the last <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in <i>pidl</i>.




## -remarks



This function does not clone the last item, so you do not have to call <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a> to release the returned pointer.



