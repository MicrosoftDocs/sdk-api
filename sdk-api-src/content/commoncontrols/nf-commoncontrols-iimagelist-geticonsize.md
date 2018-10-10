---
UID: NF:commoncontrols.IImageList.GetIconSize
title: IImageList::GetIconSize
author: windows-sdk-content
description: Gets the dimensions of images in an image list. All images in an image list have the same dimensions.
old-location: controls\IImageList_GetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\geticonsize.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetIconSize, GetIconSize method [Windows Controls], GetIconSize method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetIconSize method, IImageList.GetIconSize, IImageList::GetIconSize, comctl_IImageList_GetIconSize, comctl_IImageList_GetIconSize_cpp, commoncontrols/IImageList::GetIconSize, controls.IImageList_GetIconSize, controls.comctl_IImageList_GetIconSize
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
 - IImageList.GetIconSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::GetIconSize


## -description


Gets the dimensions of images in an image list. All images in an image list have the same dimensions. 
		


## -parameters




### -param cx [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the width, in pixels, of each image. 
				


### -param cy [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the height, in pixels, of each image. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetIconSize</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



