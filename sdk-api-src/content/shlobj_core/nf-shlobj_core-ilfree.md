---
UID: NF:shlobj_core.ILFree
title: ILFree function
author: windows-driver-content
description: Frees an ITEMIDLIST structure allocated by the Shell.
old-location: shell\ILFree.htm
old-project: shell
ms.assetid: 3457f36e-fdfd-44a4-90ca-a86f00bc9f36
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: HashTable_CoTaskMemFreeCB, ILFree, ILFree function [Windows Shell], _win32_ILFree, shell.ILFree, shlobj_core/HashTable_CoTaskMemFreeCB, shlobj_core/ILFree
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
-	ILFree
-	HashTable_CoTaskMemFreeCB
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ILFree function


## -description


Frees an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure allocated by the Shell.


## -parameters




### -param pidl [in]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be freed. This parameter can be <b>NULL</b>.


## -returns



This function does not return a value.




## -remarks



<b>ILFree</b> is often used with <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures allocated by one of the other IL functions, but it can be used to free any such structure returned by the Shell—for example, the <b>ITEMIDLIST</b> structure returned by <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> or used in a call to <a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>.

<div class="alert"><b>Note</b>  When using Windows 2000 or later, use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> rather than <b>ILFree</b>. <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures are always allocated with the Component Object Model (COM) task allocator on those platforms.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d1bb5993-fe23-42d4-a2c5-8e54e6e37d09">ILAppendID</a>



<a href="https://msdn.microsoft.com/90689575-3308-4817-ae8c-380fa5f55c88">ILClone</a>



<a href="https://msdn.microsoft.com/931df0c7-6acb-4c49-aa2b-464255e97347">ILCloneFirst</a>



<a href="https://msdn.microsoft.com/29eb1e1f-b7ac-4b72-8fce-a4388d7edfcc">ILCombine</a>
 

 

