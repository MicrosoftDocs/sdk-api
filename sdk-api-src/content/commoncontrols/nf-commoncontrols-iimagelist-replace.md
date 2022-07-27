---
UID: NF:commoncontrols.IImageList.Replace
title: IImageList::Replace (commoncontrols.h)
description: Replaces an image in an image list with a new image. (IImageList.Replace)
helpviewer_keywords: ["IImageList interface [Windows Controls]","Replace method","IImageList.Replace","IImageList::Replace","Replace","Replace method [Windows Controls]","Replace method [Windows Controls]","IImageList interface","comctl_IImageList_Replace","comctl_IImageList_Replace_cpp","commoncontrols/IImageList::Replace","controls.IImageList_Replace","controls.comctl_IImageList_Replace"]
old-location: controls\IImageList_Replace.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\replace.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],Replace method, IImageList.Replace, IImageList::Replace, Replace, Replace method [Windows Controls], Replace method [Windows Controls],IImageList interface, comctl_IImageList_Replace, comctl_IImageList_Replace_cpp, commoncontrols/IImageList::Replace, controls.IImageList_Replace, controls.comctl_IImageList_Replace
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
 - IImageList::Replace
 - commoncontrols/IImageList::Replace
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
 - IImageList.Replace
---

# IImageList::Replace


## -description

Replaces an image in an image list with a new image.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image to replace.

### -param hbmImage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the image.

### -param hbmMask [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IImageList::Replace</b> copies the bitmap to an internal data structure. You must use <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> to delete <i>hbmImage</i> and <i>hbmMask</i> after the method returns.

To use <b>IImageList::Replace</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
