---
UID: NF:ddraw.IDirectDraw7.GetVerticalBlankStatus
title: IDirectDraw7::GetVerticalBlankStatus (ddraw.h)
description: Retrieves the status of the vertical blank.
helpviewer_keywords: ["GetVerticalBlankStatus","GetVerticalBlankStatus method [DirectDraw]","GetVerticalBlankStatus method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetVerticalBlankStatus method","IDirectDraw7.GetVerticalBlankStatus","IDirectDraw7::GetVerticalBlankStatus","ddraw/IDirectDraw7::GetVerticalBlankStatus","directdraw.idirectdraw7_getverticalblankstatus"]
old-location: directdraw\idirectdraw7_getverticalblankstatus.htm
tech.root: directdraw
ms.assetid: 4bab0d24-ab11-46fb-92de-060f6afe1fde
ms.date: 12/05/2018
ms.keywords: GetVerticalBlankStatus, GetVerticalBlankStatus method [DirectDraw], GetVerticalBlankStatus method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetVerticalBlankStatus method, IDirectDraw7.GetVerticalBlankStatus, IDirectDraw7::GetVerticalBlankStatus, ddraw/IDirectDraw7::GetVerticalBlankStatus, directdraw.idirectdraw7_getverticalblankstatus
f1_keywords:
- ddraw/IDirectDraw7.GetVerticalBlankStatus
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDraw7.GetVerticalBlankStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the status of the vertical blank.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the status of the vertical blank. This parameter is TRUE if a vertical blank is occurring, and FALSE otherwise.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

To synchronize with the vertical blank, use the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-waitforverticalblank">IDirectDraw7::WaitForVerticalBlank</a> method.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>