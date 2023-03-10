---
UID: NF:ddraw.IDirectDrawClipper.SetClipList
title: IDirectDrawClipper::SetClipList (ddraw.h)
description: Sets or deletes the clip list that is used by the IDirectDrawSurface7::Blt, IDirectDrawSurface7::BltBatch, and IDirectDrawSurface7::UpdateOverlay methods on surfaces to which the parent DirectDrawClipper object is attached.
helpviewer_keywords: ["IDirectDrawClipper interface [DirectDraw]","SetClipList method","IDirectDrawClipper.SetClipList","IDirectDrawClipper::SetClipList","SetClipList","SetClipList method [DirectDraw]","SetClipList method [DirectDraw]","IDirectDrawClipper interface","ddraw/IDirectDrawClipper::SetClipList","directdraw.idirectdrawclipper_setcliplist"]
old-location: directdraw\idirectdrawclipper_setcliplist.htm
tech.root: directdraw
ms.assetid: 717f51e0-80cb-4762-b05d-30e30d065d0c
ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],SetClipList method, IDirectDrawClipper.SetClipList, IDirectDrawClipper::SetClipList, SetClipList, SetClipList method [DirectDraw], SetClipList method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::SetClipList, directdraw.idirectdrawclipper_setcliplist
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawClipper::SetClipList
 - ddraw/IDirectDrawClipper::SetClipList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawClipper.SetClipList
---

# IDirectDrawClipper::SetClipList


## -description

Sets or deletes the clip list that is used by the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a>, and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">IDirectDrawSurface7::UpdateOverlay</a> methods on surfaces to which the parent DirectDrawClipper object is attached.

## -parameters

### -param unnamedParam1 [in]

A pointer to a valid <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure for the clip list to set or NULL. If there is an existing clip list that is associated with the DirectDrawClipper object and this value is NULL, the clip list is deleted.

### -param unnamedParam2 [in]

Currently not used and must be set to 0.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CLIPPERISUSINGHWND</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

You cannot set the clip list if a window handle is already associated with the DirectDrawClipper object. 

The <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltfast">IDirectDrawSurface7::BltFast</a> method cannot clip. If you call <b>IDirectDrawSurface7::BltFast</b> on a surface with an attached clipper, it returns DDERR_UNSUPPORTED.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>