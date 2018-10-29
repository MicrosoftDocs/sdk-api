---
UID: NF:commoncontrols.IImageList.DragEnter
title: IImageList::DragEnter
author: windows-sdk-content
description: Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window.
old-location: controls\IImageList_DragEnter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragenter.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DragEnter, DragEnter method [Windows Controls], DragEnter method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragEnter method, IImageList.DragEnter, IImageList::DragEnter, comctl_IImageList_DragEnter, comctl_IImageList_DragEnter_cpp, commoncontrols/IImageList::DragEnter, controls.IImageList_DragEnter, controls.comctl_IImageList_DragEnter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.DragEnter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::DragEnter


## -description


Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. 
		


## -parameters




### -param hwndLock [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that owns the drag image.
				


### -param x [in]

Type: <b>int</b>

The x-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area.
				


### -param y [in]

Type: <b>int</b>

The y-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To begin a drag operation, use <a href="https://msdn.microsoft.com/403fede8-7b13-470d-9200-f3cc831d3132">IImageList::BeginDrag</a>. 
		

To use <b>IImageList::DragEnter</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



