---
UID: NF:shlobj_core.SHCreateShellFolderViewEx
title: SHCreateShellFolderViewEx function
author: windows-driver-content
description: Creates a new instance of the default Shell folder view object. It is recommended that you use SHCreateShellFolderView rather than this function.
old-location: shell\SHCreateShellFolderViewEx.htm
old-project: shell
ms.assetid: 7edd6786-7d74-4065-8cf1-cbb489007a46
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: SHCreateShellFolderViewEx, SHCreateShellFolderViewEx function [Windows Shell], _win32_SHCreateShellFolderViewEx, shell.SHCreateShellFolderViewEx, shlobj_core/SHCreateShellFolderViewEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHCreateShellFolderViewEx
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHCreateShellFolderViewEx function


## -description


Creates a new instance of the default Shell folder view object. It is recommended that you use <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> rather than this function.


## -parameters




### -param pcsfv [in]

Type: <b><a href="https://msdn.microsoft.com/9ec22fd4-1562-4ef0-b932-ebbf06082807">CSFV</a>*</b>

Pointer to a structure that describes the details used in creating this instance of the Shell folder view object.


### -param ppsv [out]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>**</b>

The address of an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface pointer that, when this function returns successfully, points to the new view object. On failure, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> is recommended over <b>SHCreateShellFolderViewEx</b> because of the greater flexibility of its elements to participate in various scenarios, provide new functionality to the view, and interact with other objects.

When dealing with several instances of <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>, you might want to verify which is the default Shell folder view object. To do so, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the object using IID_CDefView. This call succeeds only on the default Shell folder view object.




## -see-also




<a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>
 

 

