---
UID: NF:commoncontrols.IImageList.DragMove
title: IImageList::DragMove
author: windows-driver-content
description: Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a WM_MOUSEMOVE message.
old-location: controls\IImageList_DragMove.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\dragmove.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: DragMove, DragMove method [Windows Controls], DragMove method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],DragMove method, IImageList.DragMove, IImageList::DragMove, comctl_IImageList_DragMove, comctl_IImageList_DragMove_cpp, commoncontrols/IImageList::DragMove, controls.IImageList_DragMove, controls.comctl_IImageList_DragMove
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
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comctl32.dll
api_name:
-	IImageList.DragMove
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::DragMove


## -description


Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> message.
		


## -parameters




### -param x [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-coordinate where the drag image appears. The coordinate is relative to the upper-left corner of the window, not the client area. 
				


### -param y [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the y-coordinate where the drag image appears. The coordinate is relative to the upper-left corner of the window, not the client area. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




		To begin a drag operation, use the <a href="https://msdn.microsoft.com/403fede8-7b13-470d-9200-f3cc831d3132">IImageList::BeginDrag</a> method. 
		

To use <b>IImageList::DragMove</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



