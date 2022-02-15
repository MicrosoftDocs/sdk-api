---
UID: NF:commoncontrols.IImageList.DragLeave
title: IImageList::DragLeave (commoncontrols.h)
description: Unlocks the specified window and hides the drag image, which enables the window to update.
helpviewer_keywords: ["DragLeave","DragLeave method [Windows Controls]","DragLeave method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","DragLeave method","IImageList.DragLeave","IImageList::DragLeave","comctl_IImageList_DragLeave","comctl_IImageList_DragLeave_cpp","commoncontrols/IImageList::DragLeave","controls.IImageList_DragLeave","controls.comctl_IImageList_DragLeave"]
old-location: controls\IImageList_DragLeave.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragleave.htm
ms.date: 12/05/2018
ms.keywords: DragLeave, DragLeave method [Windows Controls], DragLeave method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragLeave method, IImageList.DragLeave, IImageList::DragLeave, comctl_IImageList_DragLeave, comctl_IImageList_DragLeave_cpp, commoncontrols/IImageList::DragLeave, controls.IImageList_DragLeave, controls.comctl_IImageList_DragLeave
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
 - IImageList::DragLeave
 - commoncontrols/IImageList::DragLeave
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
 - IImageList.DragLeave
---

# IImageList::DragLeave


## -description

Unlocks the specified window and hides the drag image, which enables the window to update.

## -parameters

### -param hwndLock [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the drag image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::DragLeave</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.