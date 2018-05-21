---
UID: NF:commoncontrols.IImageList.SetOverlayImage
title: IImageList::SetOverlayImage
author: windows-driver-content
description: Adds a specified image to the list of images used as overlay masks.
old-location: controls\IImageList_SetOverlayImage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setoverlayimage.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: IImageList interface [Windows Controls],SetOverlayImage method, IImageList.SetOverlayImage, IImageList::SetOverlayImage, SetOverlayImage, SetOverlayImage method [Windows Controls], SetOverlayImage method [Windows Controls],IImageList interface, comctl_IImageList_SetOverlayImage, comctl_IImageList_SetOverlayImage_cpp, commoncontrols/IImageList::SetOverlayImage, controls.IImageList_SetOverlayImage, controls.comctl_IImageList_SetOverlayImage
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
-	IImageList.SetOverlayImage
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::SetOverlayImage


## -description



		Adds a specified image to the list of images used as overlay masks. An image list can have up to four overlay masks in Common Controls <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 4.70</a> and earlier, and up to 15 in version 4.71 or later. The method assigns an overlay mask index to the specified image. 
		


## -parameters




### -param iImage [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the zero-based index of an image in the image list. This index identifies the image to use as an overlay mask. 
				


### -param iOverlay [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the one-based index of the overlay mask. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




		An overlay mask is an image drawn transparently over another image. To draw an overlay mask over an image, call <a href="https://msdn.microsoft.com/4a52a225-b5b3-444d-8878-a8d6de7478ee">IImageList::Draw</a>. The <b>fStyle</b> parameter of these functions can use the <a href="https://msdn.microsoft.com/6619d390-0c23-41ff-a07b-31425e47712b">INDEXTOOVERLAYMASK</a> macro to specify an overlay mask index. 
		


		A call to this method fails and returns E_INVALIDARG unless the image list is created using a mask.
		

To use <b>IImageList::SetOverlayImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



