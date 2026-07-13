---
UID: NF:commoncontrols.IImageList2.PreloadImages
title: IImageList2::PreloadImages (commoncontrols.h)
description: Preloads images, as specified.
helpviewer_keywords: ["IImageList2 interface [Windows Controls]","PreloadImages method","IImageList2.PreloadImages","IImageList2::PreloadImages","PreloadImages","PreloadImages method [Windows Controls]","PreloadImages method [Windows Controls]","IImageList2 interface","_shell_IImageList2_PreloadImages","_shell_IImageList2_PreloadImages_cpp","commoncontrols/IImageList2::PreloadImages","controls.IImageList2_PreloadImages","controls._shell_IImageList2_PreloadImages"]
old-location: controls\IImageList2_PreloadImages.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\preloadimages.htm
ms.date: 12/05/2018
ms.keywords: IImageList2 interface [Windows Controls],PreloadImages method, IImageList2.PreloadImages, IImageList2::PreloadImages, PreloadImages, PreloadImages method [Windows Controls], PreloadImages method [Windows Controls],IImageList2 interface, _shell_IImageList2_PreloadImages, _shell_IImageList2_PreloadImages_cpp, commoncontrols/IImageList2::PreloadImages, controls.IImageList2_PreloadImages, controls._shell_IImageList2_PreloadImages
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
 - IImageList2::PreloadImages
 - commoncontrols/IImageList2::PreloadImages
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
 - IImageList2.PreloadImages
---

# IImageList2::PreloadImages


## -description

Preloads images, as specified.

## -parameters

### -param pimldp [in]

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a> structure containing information about an image list draw operation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.