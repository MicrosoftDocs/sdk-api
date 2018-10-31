---
UID: NF:shlobj_core.Shell_GetImageLists
title: Shell_GetImageLists function
author: windows-sdk-content
description: Retrieves system image lists for large and small icons.
old-location: shell\Shell_GetImageLists.htm
tech.root: shell
ms.assetid: c3b73616-849c-4149-b04d-a7d389ebf700
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Shell_GetImageLists, Shell_GetImageLists function [Windows Shell], _win32_Shell_GetImageLists, shell.Shell_GetImageLists, shlobj_core/Shell_GetImageLists
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
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
 - Shell_GetImageLists
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Shell_GetImageLists function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Retrieves system image lists for large and small icons.


## -parameters




### -param phiml [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for large (32 x 32) icons.


### -param phimlSmall [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for small (16 x 16) icons.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> on success. On failure, returns <b>FALSE</b> and the image lists pointed to by <i>phiml</i> and <i>phimlSmall</i> are unchanged.




## -remarks



<div class="alert"><b>Important</b>  The image lists retrieved through this function are global system image lists; do not call <a href="https://msdn.microsoft.com/6720c9e7-b35f-4acd-8fa7-9aa9f0991879">ImageList_Destroy</a> using them.</div>
<div> </div>



## -see-also




<a href="_win32_Image_Lists">Image Lists</a>



<a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a>



<a href="https://msdn.microsoft.com/6ae80c1f-f2b7-4da9-b588-30391c8aef0e">SHGetImageList</a>
 

 

