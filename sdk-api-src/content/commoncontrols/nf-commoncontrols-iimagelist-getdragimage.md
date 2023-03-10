---
UID: NF:commoncontrols.IImageList.GetDragImage
title: IImageList::GetDragImage (commoncontrols.h)
description: Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.
helpviewer_keywords: ["GetDragImage","GetDragImage method [Windows Controls]","GetDragImage method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetDragImage method","IImageList.GetDragImage","IImageList::GetDragImage","comctl_IImageList_GetDragImage","comctl_IImageList_GetDragImage_cpp","commoncontrols/IImageList::GetDragImage","controls.IImageList_GetDragImage","controls.comctl_IImageList_GetDragImage"]
old-location: controls\IImageList_GetDragImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getdragimage.htm
ms.date: 12/05/2018
ms.keywords: GetDragImage, GetDragImage method [Windows Controls], GetDragImage method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetDragImage method, IImageList.GetDragImage, IImageList::GetDragImage, comctl_IImageList_GetDragImage, comctl_IImageList_GetDragImage_cpp, commoncontrols/IImageList::GetDragImage, controls.IImageList_GetDragImage, controls.comctl_IImageList_GetDragImage
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
 - IImageList::GetDragImage
 - commoncontrols/IImageList::GetDragImage
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
 - IImageList.GetDragImage
---

# IImageList::GetDragImage


## -description

Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.

## -parameters

### -param ppt [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the current drag position. Can be <b>NULL</b>.

### -param pptHotspot [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the offset of the drag image relative to the drag position. Can be <b>NULL</b>.

### -param riid [out]

Type: <b>REFIID</b>

An IID for the image list.

### -param ppv [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PVOID</a>*</b>

The address of a pointer to the interface for the image list if successful, <b>NULL</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The temporary image list is destroyed when <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-enddrag">IImageList::EndDrag</a> is called. To begin a drag operation, use <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-begindrag">IImageList::BeginDrag</a>. 		
		

To use <b>IImageList::GetDragImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.