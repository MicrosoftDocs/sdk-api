---
UID: NF:shlobj_core.SHCreateShellFolderView
title: SHCreateShellFolderView function
author: windows-sdk-content
description: Creates a new instance of the default Shell folder view object (DefView).
old-location: shell\SHCreateShellFolderView.htm
old-project: shell
ms.assetid: f2948a6d-84a5-456b-b328-ba76dba46e9d
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: SHCreateShellFolderView, SHCreateShellFolderView function [Windows Shell], _win32_SHCreateShellFolderView, shell.SHCreateShellFolderView, shlobj_core/SHCreateShellFolderView
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateShellFolderView
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHCreateShellFolderView function


## -description


Creates a new instance of the default Shell folder view object (DefView).


## -parameters




### -param pcsfv [in]

Type: <b>const <a href="https://msdn.microsoft.com/c6f3d9a6-5f39-4124-9340-78352f6be117">SFV_CREATE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/c6f3d9a6-5f39-4124-9340-78352f6be117">SFV_CREATE</a> structure that describes the particulars used in creating this instance of the Shell folder view object.


### -param ppsv [out]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>**</b>

When this function returns successfully, contains an interface pointer to the new <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> object. On failure, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SHCreateShellFolderView</b> is recommended over <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a> because of the greater flexibility of its elements to participate in various scenarios, provide new functionality to the view, and interact with other objects.

When dealing with several instances of <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>, you might want to verify which is the default Shell folder view object. To do so, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the object using the IID_CDefView IID. This call succeeds only when made on the default Shell folder view object.

Data sources that use the default Shell folder view object must implement these interfaces:
                
                

<ul>
<li>
<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a>
</li>
</ul>
Optionally, they can also implement <a href="https://msdn.microsoft.com/77a10997-1512-41ee-a84c-f3fa2e500d20">IPersistFolder3</a>.




## -see-also




<a href="https://msdn.microsoft.com/c6f3d9a6-5f39-4124-9340-78352f6be117">SFV_CREATE</a>



<a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a>
 

 

