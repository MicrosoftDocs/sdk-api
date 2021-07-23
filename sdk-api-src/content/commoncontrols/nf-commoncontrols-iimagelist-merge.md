---
UID: NF:commoncontrols.IImageList.Merge
title: IImageList::Merge (commoncontrols.h)
description: Creates a new image by combining two existing images. This method also creates a new image list in which to store the image.
helpviewer_keywords: ["IImageList interface [Windows Controls]","Merge method","IImageList.Merge","IImageList::Merge","Merge","Merge method [Windows Controls]","Merge method [Windows Controls]","IImageList interface","comctl_IImageList_Merge","comctl_IImageList_Merge_cpp","commoncontrols/IImageList::Merge","controls.IImageList_Merge","controls.comctl_IImageList_Merge"]
old-location: controls\IImageList_Merge.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\merge.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],Merge method, IImageList.Merge, IImageList::Merge, Merge, Merge method [Windows Controls], Merge method [Windows Controls],IImageList interface, comctl_IImageList_Merge, comctl_IImageList_Merge_cpp, commoncontrols/IImageList::Merge, controls.IImageList_Merge, controls.comctl_IImageList_Merge
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
 - IImageList::Merge
 - commoncontrols/IImageList::Merge
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
 - IImageList.Merge
---

# IImageList::Merge


## -description

Creates a new image by combining two existing images. This method also creates a new image list in which to store the image.

## -parameters

### -param i1 [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the first existing image.

### -param punk2 [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the image list that contains the second image.

### -param i2 [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the second existing image.

### -param dx [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the x-component of the offset of the second image relative to the first image.

### -param dy [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the y-component of the offset of the second image relative to the first image.

### -param riid [out]

Type: <b>REFIID</b>

An IID of the interface for the new image list.

### -param ppv [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PVOID</a>*</b>

A raw pointer to the interface for the new image list.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The new image consists of the second image drawn transparently over the first. 	The mask for the new image is obtained by combining the masks of the two existing images with the bitwise OR operator.

To use <b>IImageList::Merge</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.