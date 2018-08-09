---
UID: NF:commoncontrols.IImageList.GetOverlayImage
title: IImageList::GetOverlayImage
author: windows-sdk-content
description: Retrieves a specified image from the list of images used as overlay masks.
old-location: controls\IImageList_GetOverlayImage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getoverlayimage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetOverlayImage, GetOverlayImage method [Windows Controls], GetOverlayImage method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetOverlayImage method, IImageList.GetOverlayImage, IImageList::GetOverlayImage, comctl_IImageList_GetOverlayImage, comctl_IImageList_GetOverlayImage_cpp, commoncontrols/IImageList::GetOverlayImage, controls.IImageList_GetOverlayImage, controls.comctl_IImageList_GetOverlayImage
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
 - IImageList.GetOverlayImage
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
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



To use <b>IImageList::GetOverlayImage</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



