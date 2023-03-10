---
UID: NF:commctrl.ImageList_Create
title: ImageList_Create function (commctrl.h)
description: Creates a new image list.
helpviewer_keywords: ["ImageList_Create","ImageList_Create function [Windows Controls]","_win32_ImageList_Create","_win32_ImageList_Create_cpp","commctrl/ImageList_Create","controls.ImageList_Create","controls._win32_ImageList_Create"]
old-location: controls\ImageList_Create.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_create.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Create, ImageList_Create function [Windows Controls], _win32_ImageList_Create, _win32_ImageList_Create_cpp, commctrl/ImageList_Create, controls.ImageList_Create, controls._win32_ImageList_Create
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_Create
 - commctrl/ImageList_Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - ImageList_Create
req.apiset: ext-ms-win-shell-comctl32-init-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# ImageList_Create function


## -description

Creates a new image list.

## -parameters

### -param cx

Type: <b>int</b>

The width, in pixels, of each image.

### -param cy

Type: <b>int</b>

The height, in pixels, of each image.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A set of bit flags that specify the type of image list to create. This parameter can be a combination of the <a href="/windows/desktop/Controls/ilc-constants">Image List Creation Flags</a>.

### -param cInitial

Type: <b>int</b>

The number of images that the image list initially contains.

### -param cGrow

Type: <b>int</b>

The number of images by which the image list can grow when the system needs to make room for new images. This parameter represents the number of new images that the resized image list can contain.

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the image list if successful, or <b>NULL</b> otherwise.

## -remarks

When you finish using the image list, destroy it by calling the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_destroy">ImageList_Destroy</a> function.  

<div class="alert"><b>Note</b>  Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>
