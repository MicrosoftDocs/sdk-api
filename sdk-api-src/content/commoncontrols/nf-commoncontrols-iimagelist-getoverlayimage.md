---
UID: NF:commoncontrols.IImageList.GetOverlayImage
title: IImageList::GetOverlayImage (commoncontrols.h)
description: Retrieves a specified image from the list of images used as overlay masks.
helpviewer_keywords: ["GetOverlayImage","GetOverlayImage method [Windows Controls]","GetOverlayImage method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetOverlayImage method","IImageList.GetOverlayImage","IImageList::GetOverlayImage","comctl_IImageList_GetOverlayImage","comctl_IImageList_GetOverlayImage_cpp","commoncontrols/IImageList::GetOverlayImage","controls.IImageList_GetOverlayImage","controls.comctl_IImageList_GetOverlayImage"]
old-location: controls\IImageList_GetOverlayImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getoverlayimage.htm
ms.date: 12/05/2018
ms.keywords: GetOverlayImage, GetOverlayImage method [Windows Controls], GetOverlayImage method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetOverlayImage method, IImageList.GetOverlayImage, IImageList::GetOverlayImage, comctl_IImageList_GetOverlayImage, comctl_IImageList_GetOverlayImage_cpp, commoncontrols/IImageList::GetOverlayImage, controls.IImageList_GetOverlayImage, controls.comctl_IImageList_GetOverlayImage
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
 - IImageList::GetOverlayImage
 - commoncontrols/IImageList::GetOverlayImage
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
 - IImageList.GetOverlayImage
---

# IImageList::GetOverlayImage


## -description

Retrieves a specified image from the list of images used as overlay masks.

## -parameters

### -param iOverlay [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the one-based index of the overlay mask.

### -param piIndex [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the zero-based index of  
				an image in the image list. This index identifies the image that is used as an overlay mask.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::GetOverlayImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.