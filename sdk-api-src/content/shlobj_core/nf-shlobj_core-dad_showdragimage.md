---
UID: NF:shlobj_core.DAD_ShowDragImage
title: DAD_ShowDragImage function (shlobj_core.h)
description: Shows or hides the image being dragged. (DAD_ShowDragImage)
helpviewer_keywords: ["DAD_ShowDragImage","DAD_ShowDragImage function [Windows Shell]","FALSE","TRUE","shell.DAD_ShowDragImage","shell_DAD_ShowDragImage","shlobj_core/DAD_ShowDragImage"]
old-location: shell\DAD_ShowDragImage.htm
tech.root: shell
ms.assetid: 71448b05-9657-41e4-b5e4-6ae403219c6a
ms.date: 12/05/2018
ms.keywords: DAD_ShowDragImage, DAD_ShowDragImage function [Windows Shell], FALSE, TRUE, shell.DAD_ShowDragImage, shell_DAD_ShowDragImage, shlobj_core/DAD_ShowDragImage
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_ShowDragImage
 - shlobj_core/DAD_ShowDragImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - DAD_ShowDragImage
---

# DAD_ShowDragImage function


## -description

<p class="CCE_Message">[<b>DAD_ShowDragImage</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragshownolock">ImageList_DragShowNolock</a> instead.
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
