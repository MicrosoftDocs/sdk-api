---
UID: NF:commoncontrols.IImageList.GetBkColor
title: IImageList::GetBkColor (commoncontrols.h)
description: Gets the current background color for an image list.
helpviewer_keywords: ["GetBkColor","GetBkColor method [Windows Controls]","GetBkColor method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","GetBkColor method","IImageList.GetBkColor","IImageList::GetBkColor","comctl_IImageList_GetBkColor","comctl_IImageList_GetBkColor_cpp","commoncontrols/IImageList::GetBkColor","controls.IImageList_GetBkColor","controls.comctl_IImageList_GetBkColor"]
old-location: controls\IImageList_GetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getbkcolor.htm
ms.date: 12/05/2018
ms.keywords: GetBkColor, GetBkColor method [Windows Controls], GetBkColor method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetBkColor method, IImageList.GetBkColor, IImageList::GetBkColor, comctl_IImageList_GetBkColor, comctl_IImageList_GetBkColor_cpp, commoncontrols/IImageList::GetBkColor, controls.IImageList_GetBkColor, controls.comctl_IImageList_GetBkColor
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
 - IImageList::GetBkColor
 - commoncontrols/IImageList::GetBkColor
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
 - IImageList.GetBkColor
---

# IImageList::GetBkColor


## -description

Gets the current background color for an image list.

## -parameters

### -param pclr [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a>*</b>

A pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> that contains the background color when the method returns.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>IImageList::GetBkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.