---
UID: NF:commoncontrols.IImageList.GetImageInfo
title: IImageList::GetImageInfo (commoncontrols.h)
description: Gets information about an image.
helpviewer_keywords: ["GetImageInfo","GetImageInfo method [Windows Controls]","GetImageInfo method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetImageInfo method","IImageList.GetImageInfo","IImageList::GetImageInfo","comctl_IImageList_GetImageInfo","comctl_IImageList_GetImageInfo_cpp","commoncontrols/IImageList::GetImageInfo","controls.IImageList_GetImageInfo","controls.comctl_IImageList_GetImageInfo"]
old-location: controls\IImageList_GetImageInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimageinfo.htm
ms.date: 12/05/2018
ms.keywords: GetImageInfo, GetImageInfo method [Windows Controls], GetImageInfo method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageInfo method, IImageList.GetImageInfo, IImageList::GetImageInfo, comctl_IImageList_GetImageInfo, comctl_IImageList_GetImageInfo_cpp, commoncontrols/IImageList::GetImageInfo, controls.IImageList_GetImageInfo, controls.comctl_IImageList_GetImageInfo
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
 - IImageList::GetImageInfo
 - commoncontrols/IImageList::GetImageInfo
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
 - IImageList.GetImageInfo
---

# IImageList::GetImageInfo


## -description

Gets information about an image.

## -parameters

### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image.

### -param pImageInfo [out]

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageinfo">IMAGEINFO</a>*</b>

A pointer to an <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageinfo">IMAGEINFO</a> structure that receives information about the image. The information in this structure can directly manipulate the bitmaps of the image.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::GetImageInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.