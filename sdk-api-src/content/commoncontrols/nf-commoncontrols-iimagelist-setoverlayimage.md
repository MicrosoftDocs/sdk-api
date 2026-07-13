---
UID: NF:commoncontrols.IImageList.SetOverlayImage
title: IImageList::SetOverlayImage (commoncontrols.h)
description: Adds a specified image to the list of images used as overlay masks.
helpviewer_keywords: ["IImageList interface [Windows Controls]","SetOverlayImage method","IImageList.SetOverlayImage","IImageList::SetOverlayImage","SetOverlayImage","SetOverlayImage method [Windows Controls]","SetOverlayImage method [Windows Controls]","IImageList interface","comctl_IImageList_SetOverlayImage","comctl_IImageList_SetOverlayImage_cpp","commoncontrols/IImageList::SetOverlayImage","controls.IImageList_SetOverlayImage","controls.comctl_IImageList_SetOverlayImage"]
old-location: controls\IImageList_SetOverlayImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setoverlayimage.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],SetOverlayImage method, IImageList.SetOverlayImage, IImageList::SetOverlayImage, SetOverlayImage, SetOverlayImage method [Windows Controls], SetOverlayImage method [Windows Controls],IImageList interface, comctl_IImageList_SetOverlayImage, comctl_IImageList_SetOverlayImage_cpp, commoncontrols/IImageList::SetOverlayImage, controls.IImageList_SetOverlayImage, controls.comctl_IImageList_SetOverlayImage
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
 - IImageList::SetOverlayImage
 - commoncontrols/IImageList::SetOverlayImage
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
 - IImageList.SetOverlayImage
---

# IImageList::SetOverlayImage


## -description

Adds a specified image to the list of images used as overlay masks. An image list can have up to four overlay masks in Common Controls <a href="/windows/desktop/Controls/common-control-versions">version 4.70</a> and earlier, and up to 15 in version 4.71 or later. The method assigns an overlay mask index to the specified image.

## -parameters

### -param iImage [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the zero-based index of an image in the image list. This index identifies the image to use as an overlay mask.

### -param iOverlay [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the one-based index of the overlay mask.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An overlay mask is an image drawn transparently over another image. To draw an overlay mask over an image, call <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-draw">IImageList::Draw</a>. The <b>fStyle</b> parameter of these functions can use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro to specify an overlay mask index. 
		

A call to this method fails and returns E_INVALIDARG unless the image list is created using a mask.
		

To use <b>IImageList::SetOverlayImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.