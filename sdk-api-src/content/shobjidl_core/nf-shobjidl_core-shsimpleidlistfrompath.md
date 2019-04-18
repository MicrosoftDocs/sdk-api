---
UID: NF:shobjidl_core.SHSimpleIDListFromPath
title: SHSimpleIDListFromPath function (shobjidl_core.h)
author: windows-sdk-content
description: Deprecated. Returns a pointer to an ITEMIDLIST structure when passed a path.
old-location: shell\SHSimpleIDListFromPath.htm
tech.root: shell
ms.assetid: 349974c2-4ab9-4eb2-897d-a5934893ed07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHSimpleIDListFromPath, SHSimpleIDListFromPath function [Windows Shell], _win32_SHSimpleIDListFromPath, shell.SHSimpleIDListFromPath, shobjidl_core/SHSimpleIDListFromPath
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHSimpleIDListFromPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHSimpleIDListFromPath function


## -description


Deprecated. Returns a pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure when passed a path.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that contains the path to be converted to a PIDL.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure if successful, or <b>NULL</b> otherwise.




## -remarks



Prior to Windows 7, this function was declared in Shlobj.h. In Windows 7 and later versions, it is declared in Shobjidl.h.

<div class="alert"><b>Note</b>  This function is available through Windows 7 and Windows Server 2003. It is possible that it will not be present in future versions of Windows.</div>
<div> </div>
An alternative to this function is as follows:
                
                

<ol>
<li>Call <a href="https://msdn.microsoft.com/121cbd41-d512-4f33-b89c-d0dd9933df87">SHGetDesktopFolder</a> to obtain <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> for the desktop folder.</li>
<li>Get the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>'s bind context (<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>).</li>
<li>Call <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a> with the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> and the path.</li>
</ol>


