---
UID: NF:shlobj_core.DAD_ShowDragImage
title: DAD_ShowDragImage function
author: windows-sdk-content
description: Shows or hides the image being dragged.
old-location: shell\DAD_ShowDragImage.htm
old-project: shell
ms.assetid: 71448b05-9657-41e4-b5e4-6ae403219c6a
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: DAD_ShowDragImage, DAD_ShowDragImage function [Windows Shell], FALSE, TRUE, shell.DAD_ShowDragImage, shell_DAD_ShowDragImage, shlobj_core/DAD_ShowDragImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.redist: 
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
 - DAD_ShowDragImage
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# DAD_ShowDragImage function


## -description


<p class="CCE_Message">[<b>DAD_ShowDragImage</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/b4e4c1c0-21b4-4eb0-b38e-375eb5195816">ImageList_DragShowNolock</a> instead.
      ]

Shows or hides the image being dragged.


## -parameters




### -param fShow

Type: <b>BOOL</b>

A value that specifies whether to show or hide the image being dragged.



#### FALSE

Hides the image.



#### TRUE

Shows the image.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.




## -remarks



This function works on locked windows. It does not work on layered windows.



