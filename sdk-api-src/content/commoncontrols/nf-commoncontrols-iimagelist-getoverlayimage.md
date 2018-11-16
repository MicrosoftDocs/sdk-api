---
UID: NF:commoncontrols.IImageList.GetOverlayImage
title: IImageList::GetOverlayImage
author: windows-sdk-content
description: Retrieves a specified image from the list of images used as overlay masks.
old-location: controls\IImageList_GetOverlayImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getoverlayimage.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetOverlayImage, GetOverlayImage method [Windows Controls], GetOverlayImage method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetOverlayImage method, IImageList.GetOverlayImage, IImageList::GetOverlayImage, comctl_IImageList_GetOverlayImage, comctl_IImageList_GetOverlayImage_cpp, commoncontrols/IImageList::GetOverlayImage, controls.IImageList_GetOverlayImage, controls.comctl_IImageList_GetOverlayImage
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
 - IImageList.GetOverlayImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- commoncontrols.h
: 
- IImageList.GetOverlayImage
: 
---

# IImageList::GetOverlayImage


## -description


Retrieves a specified image from the list of images used as overlay masks. 
		


## -parameters




### -param iOverlay [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the one-based index of the overlay mask. 


### -param piIndex [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the zero-based index of  
				an image in the image list. This index identifies the image that is used as an overlay mask. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetOverlayImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



