---
UID: NF:commoncontrols.IImageList.SetDragCursorImage
title: IImageList::SetDragCursorImage
author: windows-sdk-content
description: Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image.
old-location: controls\IImageList_SetDragCursorImage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setdragcursorimage.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IImageList interface [Windows Controls],SetDragCursorImage method, IImageList.SetDragCursorImage, IImageList::SetDragCursorImage, SetDragCursorImage, SetDragCursorImage method [Windows Controls], SetDragCursorImage method [Windows Controls],IImageList interface, comctl_IImageList_SetDragCursorImage, comctl_IImageList_SetDragCursorImage_cpp, commoncontrols/IImageList::SetDragCursorImage, controls.IImageList_SetDragCursorImage, controls.comctl_IImageList_SetDragCursorImage
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
 - IImageList.SetDragCursorImage
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::SetDragCursorImage


## -description



		Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image. 
		


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that accesses the image list interface, which contains the new image to combine with the drag image. 
				


### -param iDrag [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the new image to combine with the drag image. 
				


### -param dxHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-component of the hot spot within the new image. 
				


### -param dyHotspot [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the x-component of the hot spot within the new image. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::SetDragCursorImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



