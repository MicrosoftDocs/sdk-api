---
UID: NF:commoncontrols.IImageList.Add
title: IImageList::Add (commoncontrols.h)
description: Adds an image or images to an image list. (IImageList.Add)
helpviewer_keywords: ["Add","Add method [Windows Controls]","Add method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","Add method","IImageList.Add","IImageList::Add","comctl_IImageList_Add","comctl_IImageList_Add_cpp","commoncontrols/IImageList::Add","controls.IImageList_Add","controls.comctl_IImageList_Add"]
old-location: controls\IImageList_Add.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\add.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Controls], Add method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],Add method, IImageList.Add, IImageList::Add, comctl_IImageList_Add, comctl_IImageList_Add_cpp, commoncontrols/IImageList::Add, controls.IImageList_Add, controls.comctl_IImageList_Add
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IImageList::Add
 - commoncontrols/IImageList::Add
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
 - IImageList.Add
---

# IImageList::Add


## -description

Adds an image or images to an image list.

## -parameters

### -param hbmImage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the image or images. The number of images is inferred from the width of the bitmap.

### -param hbmMask [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored.

### -param pi [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the index of the first new image. If the method fails to successfully add the new image, this value is -1.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IImageList::Add</b> copies the bitmap to an internal data structure. You must use the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete <i>hbmImage</i> and <i>hbmMask</i> after the method returns.

To use <b>IImageList::Add</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
