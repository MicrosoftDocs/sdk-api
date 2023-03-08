---
UID: NF:commoncontrols.IImageList.Draw
title: IImageList::Draw (commoncontrols.h)
description: Draws an image list item in the specified device context. (IImageList.Draw)
helpviewer_keywords: ["Draw","Draw method [Windows Controls]","Draw method [Windows Controls]","IImageList interface","IImageList interface [Windows Controls]","Draw method","IImageList.Draw","IImageList::Draw","comctl_IImageList_Draw","comctl_IImageList_Draw_cpp","commoncontrols/IImageList::Draw","controls.IImageList_Draw","controls.comctl_IImageList_Draw"]
old-location: controls\IImageList_Draw.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\draw.htm
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Windows Controls], Draw method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],Draw method, IImageList.Draw, IImageList::Draw, comctl_IImageList_Draw, comctl_IImageList_Draw_cpp, commoncontrols/IImageList::Draw, controls.IImageList_Draw, controls.comctl_IImageList_Draw
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
 - IImageList::Draw
 - commoncontrols/IImageList::Draw
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
 - IImageList.Draw
---

# IImageList::Draw


## -description

Draws an image list item in the specified device context.

## -parameters

### -param pimldp [in]

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an  <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a> structure that contains the  drawing parameters.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Overlay images draw transparently over the primary image specified in the <b>i</b> parameter of <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imagelistdrawparams">IMAGELISTDRAWPARAMS</a>. You specify an overlay image in the <b>fStyle</b>, parameter of <b>IMAGELISTDRAWPARAMS</b> using the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro to shift the one-based index of the overlay image. Use the OR operator to combine the macro's return value with the drawing style flags specified in <b>fStyle</b>. You must first specify this image as an overlay image by using <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-setoverlayimage">IImageList::SetOverlayImage</a>. 
		

To use <b>IImageList::Draw</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
