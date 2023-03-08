---
UID: NF:commoncontrols.IImageList.DragEnter
title: IImageList::DragEnter (commoncontrols.h)
description: Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. (IImageList.DragEnter)
helpviewer_keywords: ["DragEnter","DragEnter method [Windows Controls]","DragEnter method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","DragEnter method","IImageList.DragEnter","IImageList::DragEnter","comctl_IImageList_DragEnter","comctl_IImageList_DragEnter_cpp","commoncontrols/IImageList::DragEnter","controls.IImageList_DragEnter","controls.comctl_IImageList_DragEnter"]
old-location: controls\IImageList_DragEnter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragenter.htm
ms.date: 12/05/2018
ms.keywords: DragEnter, DragEnter method [Windows Controls], DragEnter method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragEnter method, IImageList.DragEnter, IImageList::DragEnter, comctl_IImageList_DragEnter, comctl_IImageList_DragEnter_cpp, commoncontrols/IImageList::DragEnter, controls.IImageList_DragEnter, controls.comctl_IImageList_DragEnter
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
 - IImageList::DragEnter
 - commoncontrols/IImageList::DragEnter
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
 - IImageList.DragEnter
---

# IImageList::DragEnter


## -description

Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window.

## -parameters

### -param hwndLock [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that owns the drag image.

### -param x [in]

Type: <b>int</b>

The x-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area.

### -param y [in]

Type: <b>int</b>

The y-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To begin a drag operation, use <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-begindrag">IImageList::BeginDrag</a>. 
		

To use <b>IImageList::DragEnter</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
