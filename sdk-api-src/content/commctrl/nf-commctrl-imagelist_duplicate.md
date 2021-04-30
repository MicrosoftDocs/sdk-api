---
UID: NF:commctrl.ImageList_Duplicate
title: ImageList_Duplicate function (commctrl.h)
description: Creates a duplicate of an existing image list.
helpviewer_keywords: ["ImageList_Duplicate","ImageList_Duplicate function [Windows Controls]","_win32_ImageList_Duplicate","_win32_ImageList_Duplicate_cpp","commctrl/ImageList_Duplicate","controls.ImageList_Duplicate","controls._win32_ImageList_Duplicate"]
old-location: controls\ImageList_Duplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_duplicate.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Duplicate, ImageList_Duplicate function [Windows Controls], _win32_ImageList_Duplicate, _win32_ImageList_Duplicate_cpp, commctrl/ImageList_Duplicate, controls.ImageList_Duplicate, controls._win32_ImageList_Duplicate
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
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_Duplicate
 - commctrl/ImageList_Duplicate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_Duplicate
---

# ImageList_Duplicate function


## -description

Creates a duplicate of an existing image list.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list to be duplicated. All information contained in the original image list for normal images is copied to the new image list. Overlay images are not copied.

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the new duplicate image list if successful, or <b>NULL</b> otherwise.

