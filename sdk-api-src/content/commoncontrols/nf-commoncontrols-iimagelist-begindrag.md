---
UID: NF:commoncontrols.IImageList.BeginDrag
title: IImageList::BeginDrag (commoncontrols.h)
description: Begins dragging an image. (IImageList.BeginDrag)
helpviewer_keywords: ["BeginDrag","BeginDrag method [Windows Controls]","BeginDrag method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","BeginDrag method","IImageList.BeginDrag","IImageList::BeginDrag","comctl_IImageList_BeginDrag","comctl_IImageList_BeginDrag_cpp","commoncontrols/IImageList::BeginDrag","controls.IImageList_BeginDrag","controls.comctl_IImageList_BeginDrag"]
old-location: controls\IImageList_BeginDrag.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\begindrag.htm
ms.date: 12/05/2018
ms.keywords: BeginDrag, BeginDrag method [Windows Controls], BeginDrag method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],BeginDrag method, IImageList.BeginDrag, IImageList::BeginDrag, comctl_IImageList_BeginDrag, comctl_IImageList_BeginDrag_cpp, commoncontrols/IImageList::BeginDrag, controls.IImageList_BeginDrag, controls.comctl_IImageList_BeginDrag
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
 - IImageList::BeginDrag
 - commoncontrols/IImageList::BeginDrag
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
 - IImageList.BeginDrag
---

# IImageList::BeginDrag


## -description

Begins dragging an image.

## -parameters

### -param iTrack [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image to drag.

### -param dxHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-component of the drag position relative to the upper-left corner of the image.

### -param dyHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the y-component of the drag position relative to the upper-left corner of the image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IImageList::BeginDrag</b> creates a temporary image list that is used for dragging. In response to subsequent <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> messages, you can move the drag image by using <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-dragmove">IImageList::DragMove</a>. To end the drag operation, you can use <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-enddrag">IImageList::EndDrag</a>. 
		

To use <b>IImageList::BeginDrag</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
