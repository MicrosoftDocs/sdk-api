---
UID: NF:shlobj_core.SHCloneSpecialIDList
title: SHCloneSpecialIDList function
author: windows-sdk-content
description: SHCloneSpecialIDList may be altered or unavailable. Instead, use SHGetSpecialFolderLocation.
old-location: shell\SHCloneSpecialIDList.htm
old-project: shell
ms.assetid: ef8a6168-c495-47a7-af97-dfee19a41f64
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHCloneSpecialIDList, SHCloneSpecialIDList function [Windows Shell], _win32_SHCloneSpecialIDList, shell.SHCloneSpecialIDList, shlobj_core/SHCloneSpecialIDList
ms.prod: windows
ms.technology: windows-sdk
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
api_name:
-	SHCloneSpecialIDList
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHCloneSpecialIDList function


## -description


<p class="CCE_Message">[<b>SHCloneSpecialIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/10b00497-fc3b-4e34-acd8-bc0721c0dc05">SHGetSpecialFolderLocation</a>.]

Retrieves a pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that specifies a special folder.


## -parameters




### -param hwnd

TBD


### -param csidl [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that identifies the folder of interest.


### -param fCreate [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates if the folder should be created if it does not already exist. If  <i>fCreate</i> is <b>TRUE</b>, the folder is created. If it is <b>FALSE</b>, the folder is not created.


#### - hwndOwner

Type: <b>HWND</b>

Reserved.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure of a special folder specified by <i>csidl</i>. The function creates the folder if <i>fCreate</i> is <b>TRUE</b>.




## -remarks



When finished, you should free the pointer to the cloned folder with <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a>.



