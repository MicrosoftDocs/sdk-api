---
UID: NF:commoncontrols.IImageList.DragShowNolock
title: IImageList::DragShowNolock (commoncontrols.h)
description: Shows or hides the image being dragged. (IImageList.DragShowNolock)
helpviewer_keywords: ["DragShowNolock","DragShowNolock method [Windows Controls]","DragShowNolock method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","DragShowNolock method","IImageList.DragShowNolock","IImageList::DragShowNolock","comctl_IImageList_DragShowNolock","comctl_IImageList_DragShowNolock_cpp","commoncontrols/IImageList::DragShowNolock","controls.IImageList_DragShowNolock","controls.comctl_IImageList_DragShowNolock"]
old-location: controls\IImageList_DragShowNolock.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragshownolock.htm
ms.date: 12/05/2018
ms.keywords: DragShowNolock, DragShowNolock method [Windows Controls], DragShowNolock method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragShowNolock method, IImageList.DragShowNolock, IImageList::DragShowNolock, comctl_IImageList_DragShowNolock, comctl_IImageList_DragShowNolock_cpp, commoncontrols/IImageList::DragShowNolock, controls.IImageList_DragShowNolock, controls.comctl_IImageList_DragShowNolock
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
 - IImageList::DragShowNolock
 - commoncontrols/IImageList::DragShowNolock
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
 - IImageList.DragShowNolock
---

# IImageList::DragShowNolock


## -description

Shows or hides the image being dragged.

## -parameters

### -param fShow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value that specifies whether to show or hide the image being dragged. Specify <b>TRUE</b> to show the image or <b>FALSE</b> to hide the image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::DragShowNolock</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
