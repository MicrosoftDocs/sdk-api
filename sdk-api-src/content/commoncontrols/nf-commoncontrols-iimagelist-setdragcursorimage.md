---
UID: NF:commoncontrols.IImageList.SetDragCursorImage
title: IImageList::SetDragCursorImage (commoncontrols.h)
description: Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image.
helpviewer_keywords: ["IImageList interface [Windows Controls]","SetDragCursorImage method","IImageList.SetDragCursorImage","IImageList::SetDragCursorImage","SetDragCursorImage","SetDragCursorImage method [Windows Controls]","SetDragCursorImage method [Windows Controls]","IImageList interface","comctl_IImageList_SetDragCursorImage","comctl_IImageList_SetDragCursorImage_cpp","commoncontrols/IImageList::SetDragCursorImage","controls.IImageList_SetDragCursorImage","controls.comctl_IImageList_SetDragCursorImage"]
old-location: controls\IImageList_SetDragCursorImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setdragcursorimage.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],SetDragCursorImage method, IImageList.SetDragCursorImage, IImageList::SetDragCursorImage, SetDragCursorImage, SetDragCursorImage method [Windows Controls], SetDragCursorImage method [Windows Controls],IImageList interface, comctl_IImageList_SetDragCursorImage, comctl_IImageList_SetDragCursorImage_cpp, commoncontrols/IImageList::SetDragCursorImage, controls.IImageList_SetDragCursorImage, controls.comctl_IImageList_SetDragCursorImage
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList::SetDragCursorImage
 - commoncontrols/IImageList::SetDragCursorImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.SetDragCursorImage
---

# IImageList::SetDragCursorImage


## -description

Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that accesses the image list interface, which contains the new image to combine with the drag image.

### -param iDrag [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the new image to combine with the drag image.

### -param dxHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-component of the hot spot within the new image.

### -param dyHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-component of the hot spot within the new image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::SetDragCursorImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.