---
UID: NF:commctrl.ImageList_ReplaceIcon
title: ImageList_ReplaceIcon function
author: windows-sdk-content
description: Replaces an image with an icon or cursor.
old-location: controls\ImageList_ReplaceIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_replaceicon.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ImageList_ReplaceIcon, ImageList_ReplaceIcon function [Windows Controls], _win32_ImageList_ReplaceIcon, _win32_ImageList_ReplaceIcon_cpp, commctrl/ImageList_ReplaceIcon, controls.ImageList_ReplaceIcon, controls._win32_ImageList_ReplaceIcon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - ImageList_ReplaceIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_ReplaceIcon function


## -description


Replaces an image with an icon or cursor.


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i [in]

Type: <b>int</b>

The index of the image to replace. If 
					<i>i</i> is -1, the function appends the image to the end of the list. 


### -param hicon [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HICON</a></b>

The handle to the icon or cursor that contains the bitmap and mask for the new image. 


## -returns



Type: <b>int</b>

Returns the index of the image if successful, or -1 otherwise.




## -remarks



Because the system does not save 
				<i>hicon</i>, you can destroy it after the function returns if the icon or cursor was created by the <a href="https://msdn.microsoft.com/en-us/library/ms648059(v=VS.85).aspx">CreateIcon</a> function. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 



