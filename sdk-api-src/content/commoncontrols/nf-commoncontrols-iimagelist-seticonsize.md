---
UID: NF:commoncontrols.IImageList.SetIconSize
title: IImageList::SetIconSize
author: windows-sdk-content
description: Sets the dimensions of images in an image list and removes all images from the list.
old-location: controls\IImageList_SetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\seticonsize.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IImageList interface [Windows Controls],SetIconSize method, IImageList.SetIconSize, IImageList::SetIconSize, SetIconSize, SetIconSize method [Windows Controls], SetIconSize method [Windows Controls],IImageList interface, comctl_IImageList_SetIconSize, comctl_IImageList_SetIconSize_cpp, commoncontrols/IImageList::SetIconSize, controls.IImageList_SetIconSize, controls.comctl_IImageList_SetIconSize
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
 - IImageList.SetIconSize
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
- IImageList.SetIconSize
: 
---

# IImageList::SetIconSize


## -description


Sets the dimensions of images in an image list and removes all images from the list. 
		


## -parameters




### -param cx [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the width, in pixels, of the images in the image list. All images in an image list have the same dimensions. 
				


### -param cy [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the height, in pixels, of the images in the image list. All images in an image list have the same dimensions. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::SetIconSize</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



