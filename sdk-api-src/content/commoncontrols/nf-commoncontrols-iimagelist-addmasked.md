---
UID: NF:commoncontrols.IImageList.AddMasked
title: IImageList::AddMasked (commoncontrols.h)
description: Adds an image or images to an image list, generating a mask from the specified bitmap. (IImageList.AddMasked)
helpviewer_keywords: ["AddMasked","AddMasked method [Windows Controls]","AddMasked method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","AddMasked method","IImageList.AddMasked","IImageList::AddMasked","comctl_IImageList_AddMasked","comctl_IImageList_AddMasked_cpp","commoncontrols/IImageList::AddMasked","controls.IImageList_AddMasked","controls.comctl_IImageList_AddMasked"]
old-location: controls\IImageList_AddMasked.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\addmasked.htm
ms.date: 12/05/2018
ms.keywords: AddMasked, AddMasked method [Windows Controls], AddMasked method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],AddMasked method, IImageList.AddMasked, IImageList::AddMasked, comctl_IImageList_AddMasked, comctl_IImageList_AddMasked_cpp, commoncontrols/IImageList::AddMasked, controls.IImageList_AddMasked, controls.comctl_IImageList_AddMasked
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
 - IImageList::AddMasked
 - commoncontrols/IImageList::AddMasked
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
 - IImageList.AddMasked
---

# IImageList::AddMasked


## -description

Adds an image or images to an image list, generating a mask from the specified bitmap.

## -parameters

### -param hbmImage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains one or more images. The number of images is inferred from the width of the bitmap.

### -param crMask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The color used to generate the mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is CLR_DEFAULT, then the color of the pixel at (0,0) is used as the mask.

### -param pi [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that contains the index of the first new image when it returns, if successful, or -1 otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  The bitmap passed in <i>hbmImage</i> will be modified.</div>
<div> </div>
<b>IImageList::AddMasked</b> copies the bitmap to an internal data structure. Bitmaps with color depth greater than 8bpp are not supported. You must use the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete <i>hbmImage</i> and <i>crMask</i> after the method returns. 
        

To use <b>IImageList::AddMasked</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
