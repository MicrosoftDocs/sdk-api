---
UID: NF:commoncontrols.IImageList.GetImageRect
title: IImageList::GetImageRect (commoncontrols.h)
description: Gets an image's bounding rectangle.
helpviewer_keywords: ["GetImageRect","GetImageRect method [Windows Controls]","GetImageRect method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetImageRect method","IImageList.GetImageRect","IImageList::GetImageRect","comctl_IImageList_GetImageRect","comctl_IImageList_GetImageRect_cpp","commoncontrols/IImageList::GetImageRect","controls.IImageList_GetImageRect","controls.comctl_IImageList_GetImageRect"]
old-location: controls\IImageList_GetImageRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimagerect.htm
ms.date: 12/05/2018
ms.keywords: GetImageRect, GetImageRect method [Windows Controls], GetImageRect method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageRect method, IImageList.GetImageRect, IImageList::GetImageRect, comctl_IImageList_GetImageRect, comctl_IImageList_GetImageRect_cpp, commoncontrols/IImageList::GetImageRect, controls.IImageList_GetImageRect, controls.comctl_IImageList_GetImageRect
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
 - IImageList::GetImageRect
 - commoncontrols/IImageList::GetImageRect
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
 - IImageList.GetImageRect
---

# IImageList::GetImageRect


## -description

Gets an image's bounding rectangle.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image.

### -param prc [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b> RECT</b> that contains the bounding rectangle when the method returns.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::GetImageRect</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.