---
UID: NF:commoncontrols.IImageList.GetIconSize
title: IImageList::GetIconSize (commoncontrols.h)
description: Gets the dimensions of images in an image list. All images in an image list have the same dimensions.
helpviewer_keywords: ["GetIconSize","GetIconSize method [Windows Controls]","GetIconSize method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetIconSize method","IImageList.GetIconSize","IImageList::GetIconSize","comctl_IImageList_GetIconSize","comctl_IImageList_GetIconSize_cpp","commoncontrols/IImageList::GetIconSize","controls.IImageList_GetIconSize","controls.comctl_IImageList_GetIconSize"]
old-location: controls\IImageList_GetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\geticonsize.htm
ms.date: 12/05/2018
ms.keywords: GetIconSize, GetIconSize method [Windows Controls], GetIconSize method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetIconSize method, IImageList.GetIconSize, IImageList::GetIconSize, comctl_IImageList_GetIconSize, comctl_IImageList_GetIconSize_cpp, commoncontrols/IImageList::GetIconSize, controls.IImageList_GetIconSize, controls.comctl_IImageList_GetIconSize
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
 - IImageList::GetIconSize
 - commoncontrols/IImageList::GetIconSize
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
 - IImageList.GetIconSize
---

# IImageList::GetIconSize


## -description

Gets the dimensions of images in an image list. All images in an image list have the same dimensions.

## -parameters

### -param cx [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the width, in pixels, of each image.

### -param cy [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the height, in pixels, of each image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::GetIconSize</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.