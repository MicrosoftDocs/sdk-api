---
UID: NF:commoncontrols.IImageList.SetIconSize
title: IImageList::SetIconSize (commoncontrols.h)
description: Sets the dimensions of images in an image list and removes all images from the list.helpviewer_keywords: ["IImageList interface [Windows Controls]","SetIconSize method","IImageList.SetIconSize","IImageList::SetIconSize","SetIconSize","SetIconSize method [Windows Controls]","SetIconSize method [Windows Controls]","IImageList interface","comctl_IImageList_SetIconSize","comctl_IImageList_SetIconSize_cpp","commoncontrols/IImageList::SetIconSize","controls.IImageList_SetIconSize","controls.comctl_IImageList_SetIconSize"]
old-location: controls\IImageList_SetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\seticonsize.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],SetIconSize method, IImageList.SetIconSize, IImageList::SetIconSize, SetIconSize, SetIconSize method [Windows Controls], SetIconSize method [Windows Controls],IImageList interface, comctl_IImageList_SetIconSize, comctl_IImageList_SetIconSize_cpp, commoncontrols/IImageList::SetIconSize, controls.IImageList_SetIconSize, controls.comctl_IImageList_SetIconSize
f1_keywords:
- commoncontrols/IImageList.SetIconSize
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::SetIconSize</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



