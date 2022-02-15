---
UID: NF:commoncontrols.IImageList.SetBkColor
title: IImageList::SetBkColor (commoncontrols.h)
description: Sets the background color for an image list.
helpviewer_keywords: ["IImageList interface [Windows Controls]","SetBkColor method","IImageList.SetBkColor","IImageList::SetBkColor","SetBkColor","SetBkColor method [Windows Controls]","SetBkColor method [Windows Controls]","IImageList interface","comctl_IImageList_SetBkColor","comctl_IImageList_SetBkColor_cpp","commoncontrols/IImageList::SetBkColor","controls.IImageList_SetBkColor","controls.comctl_IImageList_SetBkColor"]
old-location: controls\IImageList_SetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setbkcolor.htm
ms.date: 12/05/2018
ms.keywords: IImageList interface [Windows Controls],SetBkColor method, IImageList.SetBkColor, IImageList::SetBkColor, SetBkColor, SetBkColor method [Windows Controls], SetBkColor method [Windows Controls],IImageList interface, comctl_IImageList_SetBkColor, comctl_IImageList_SetBkColor_cpp, commoncontrols/IImageList::SetBkColor, controls.IImageList_SetBkColor, controls.comctl_IImageList_SetBkColor
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
 - IImageList::SetBkColor
 - commoncontrols/IImageList::SetBkColor
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
 - IImageList.SetBkColor
---

# IImageList::SetBkColor


## -description

Sets the background color for an image list. This method only functions if you add an icon to the image list or use the <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-addmasked">IImageList::AddMasked</a> method to add a black and white bitmap. Without a mask, the entire image draws, and the background color is not visible.

## -parameters

### -param clrBk [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The background color to set. If this parameter is set to CLR_NONE, then images draw transparently using the <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-addmasked">mask</a>.

### -param pclr [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a>*</b>

A pointer to a <b>COLORREF</b> that contains the previous background color on return if successful, or CLR_NONE otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::SetBkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.