---
UID: NF:commoncontrols.IImageList2.ReplaceFromImageList
title: IImageList2::ReplaceFromImageList (commoncontrols.h)
description: Replaces an image in one image list with an image from another image list.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","ReplaceFromImageList method","IImageList2.ReplaceFromImageList","IImageList2::ReplaceFromImageList","ReplaceFromImageList","ReplaceFromImageList method [Windows Controls]","ReplaceFromImageList method [Windows Controls]","IImageList2 interface","_shell_IImageList2_ReplaceFromImageList","_shell_IImageList2_ReplaceFromImageList_cpp","commoncontrols/IImageList2::ReplaceFromImageList","controls.IImageList2_ReplaceFromImageList","controls._shell_IImageList2_ReplaceFromImageList"]
old-location: controls\IImageList2_ReplaceFromImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\replacefromimagelist.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],ReplaceFromImageList method, IImageList2.ReplaceFromImageList, IImageList2::ReplaceFromImageList, ReplaceFromImageList, ReplaceFromImageList method [Windows Controls], ReplaceFromImageList method [Windows Controls],IImageList2 interface, _shell_IImageList2_ReplaceFromImageList, _shell_IImageList2_ReplaceFromImageList_cpp, commoncontrols/IImageList2::ReplaceFromImageList, controls.IImageList2_ReplaceFromImageList, controls._shell_IImageList2_ReplaceFromImageList
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
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
 - IImageList2::ReplaceFromImageList
 - commoncontrols/IImageList2::ReplaceFromImageList
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
 - IImageList2.ReplaceFromImageList
---

# IImageList2::ReplaceFromImageList


## -description

Replaces an image in one image list with an image from another image list.

## -parameters

### -param i [in]

Type: <b>int</b>

The index of the destination image in the image list. This is the image that is overwritten by the new image.

### -param pil [in]

Type: <b><a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">IImageList</a>*</b>

A pointer to the source image list.

### -param iSrc [in]

Type: <b>int</b>

The index of the source image in the image list pointed to by <i>pil</i>.

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Not used; must be 0.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.