---
UID: NF:commoncontrols.IImageList.DragMove
title: IImageList::DragMove (commoncontrols.h)
description: Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a WM_MOUSEMOVE message. (IImageList.DragMove)
helpviewer_keywords: ["DragMove","DragMove method [Windows Controls]","DragMove method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","DragMove method","IImageList.DragMove","IImageList::DragMove","comctl_IImageList_DragMove","comctl_IImageList_DragMove_cpp","commoncontrols/IImageList::DragMove","controls.IImageList_DragMove","controls.comctl_IImageList_DragMove"]
old-location: controls\IImageList_DragMove.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragmove.htm
ms.date: 12/05/2018
ms.keywords: DragMove, DragMove method [Windows Controls], DragMove method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragMove method, IImageList.DragMove, IImageList::DragMove, comctl_IImageList_DragMove, comctl_IImageList_DragMove_cpp, commoncontrols/IImageList::DragMove, controls.IImageList_DragMove, controls.comctl_IImageList_DragMove
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
 - IImageList::DragMove
 - commoncontrols/IImageList::DragMove
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
 - IImageList.DragMove
---

# IImageList::DragMove


## -description

Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> message.

## -parameters

### -param x [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-coordinate where the drag image appears. The coordinate is relative to the upper-left corner of the window, not the client area.

### -param y [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the y-coordinate where the drag image appears. The coordinate is relative to the upper-left corner of the window, not the client area.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To begin a drag operation, use the <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-begindrag">IImageList::BeginDrag</a> method. 
		

To use <b>IImageList::DragMove</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
