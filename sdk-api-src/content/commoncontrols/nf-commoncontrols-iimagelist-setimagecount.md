---
UID: NF:commoncontrols.IImageList.SetImageCount
title: IImageList::SetImageCount (commoncontrols.h)
description: Resizes an existing image list. (IImageList.SetImageCount)
helpviewer_keywords: ["IImageList interface [Windows Controls]","SetImageCount method","IImageList.SetImageCount","IImageList::SetImageCount","SetImageCount","SetImageCount method [Windows Controls]","SetImageCount method [Windows Controls]","IImageList interface","comctl_IImageList_SetImageCount","comctl_IImageList_SetImageCount_cpp","commoncontrols/IImageList::SetImageCount","controls.IImageList_SetImageCount","controls.comctl_IImageList_SetImageCount"]
old-location: controls\IImageList_SetImageCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setimagecount.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],SetImageCount method, IImageList.SetImageCount, IImageList::SetImageCount, SetImageCount, SetImageCount method [Windows Controls], SetImageCount method [Windows Controls],IImageList interface, comctl_IImageList_SetImageCount, comctl_IImageList_SetImageCount_cpp, commoncontrols/IImageList::SetImageCount, controls.IImageList_SetImageCount, controls.comctl_IImageList_SetImageCount
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
 - IImageList::SetImageCount
 - commoncontrols/IImageList::SetImageCount
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
 - IImageList.SetImageCount
---

# IImageList::SetImageCount


## -description

Resizes an existing image list.

## -parameters

### -param uNewCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that specifies the new size of the image list.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an application expands an image list using this method, it must add new images by using <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-replace">IImageList::Replace</a>. If the application does not add valid images to the new indexes, draw operations that use the new indexes are unpredictable. 
		

If you decrease the size of an image list using this method, images at the end of the list for which there is no longer room are truncated from the list.  Images truncated in this manner are automatically deallocated. 

To use <b>IImageList::SetImageCount</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
