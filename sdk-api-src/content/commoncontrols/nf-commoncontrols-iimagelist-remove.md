---
UID: NF:commoncontrols.IImageList.Remove
title: IImageList::Remove (commoncontrols.h)
description: Removes an image from an image list. (IImageList.Remove)
helpviewer_keywords: ["IImageList interface [Windows Controls]","Remove method","IImageList.Remove","IImageList::Remove","Remove","Remove method [Windows Controls]","Remove method [Windows Controls]","IImageList interface","comctl_IImageList_Remove","comctl_IImageList_Remove_cpp","commoncontrols/IImageList::Remove","controls.IImageList_Remove","controls.comctl_IImageList_Remove"]
old-location: controls\IImageList_Remove.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\remove.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],Remove method, IImageList.Remove, IImageList::Remove, Remove, Remove method [Windows Controls], Remove method [Windows Controls],IImageList interface, comctl_IImageList_Remove, comctl_IImageList_Remove_cpp, commoncontrols/IImageList::Remove, controls.IImageList_Remove, controls.comctl_IImageList_Remove
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList::Remove
 - commoncontrols/IImageList::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.Remove
---

# IImageList::Remove


## -description

Removes an image from an image list.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b>  that contains the index of the image to remove. If this parameter is -1, the method removes all images.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When an image is removed, the indexes of the remaining images adjust so that they  always range from zero to one less than the number of images in the image list. For example, if you remove the image at index 0, then image 1 becomes image 0, image 2 becomes image 1, and so on. 
		

To use <b>IImageList::Remove</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
