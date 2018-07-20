---
UID: NF:commoncontrols.IImageList.BeginDrag
title: IImageList::BeginDrag
author: windows-sdk-content
description: Begins dragging an image.
old-location: controls\IImageList_BeginDrag.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\begindrag.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: BeginDrag, BeginDrag method [Windows Controls], BeginDrag method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],BeginDrag method, IImageList.BeginDrag, IImageList::BeginDrag, comctl_IImageList_BeginDrag, comctl_IImageList_BeginDrag_cpp, commoncontrols/IImageList::BeginDrag, controls.IImageList_BeginDrag, controls.comctl_IImageList_BeginDrag
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.BeginDrag
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IImageList::BeginDrag</b> creates a temporary image list that is used for dragging. In response to subsequent <a href="https://msdn.microsoft.com/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> messages, you can move the drag image by using <a href="https://msdn.microsoft.com/library/Bb761451(v=VS.85).aspx">IImageList::DragMove</a>. To end the drag operation, you can use <a href="https://msdn.microsoft.com/library/Bb761457(v=VS.85).aspx">IImageList::EndDrag</a>. 
		

To use <b>IImageList::BeginDrag</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



