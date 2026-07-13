---
UID: NF:commctrl.ImageList_RemoveAll
title: ImageList_RemoveAll macro (commctrl.h)
description: Calls the ImageList_Remove function to remove all of the images from an image list.
helpviewer_keywords: ["ImageList_RemoveAll","ImageList_RemoveAll macro [Windows Controls]","_win32_ImageList_RemoveAll","_win32_ImageList_RemoveAll_cpp","commctrl/ImageList_RemoveAll","controls.ImageList_RemoveAll","controls._win32_ImageList_RemoveAll"]
old-location: controls\ImageList_RemoveAll.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_removeall.htm
ms.date: 10/21/2024
ms.keywords: ImageList_RemoveAll, ImageList_RemoveAll macro [Windows Controls], _win32_ImageList_RemoveAll, _win32_ImageList_RemoveAll_cpp, commctrl/ImageList_RemoveAll, controls.ImageList_RemoveAll, controls._win32_ImageList_RemoveAll
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_RemoveAll
 - commctrl/ImageList_RemoveAll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ImageList_RemoveAll
---

# ImageList_RemoveAll macro

## -syntax

```cpp
BOOL ImageList_RemoveAll(
   HIMAGELIST himl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Calls the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_remove">ImageList_Remove</a> function to remove all of the images from an image list.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.
