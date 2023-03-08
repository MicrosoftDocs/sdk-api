---
UID: NF:ddraw.IDirectDrawClipper.IsClipListChanged
title: IDirectDrawClipper::IsClipListChanged (ddraw.h)
description: Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.
helpviewer_keywords: ["IDirectDrawClipper interface [DirectDraw]","IsClipListChanged method","IDirectDrawClipper.IsClipListChanged","IDirectDrawClipper::IsClipListChanged","IsClipListChanged","IsClipListChanged method [DirectDraw]","IsClipListChanged method [DirectDraw]","IDirectDrawClipper interface","ddraw/IDirectDrawClipper::IsClipListChanged","directdraw.idirectdrawclipper_iscliplistchanged"]
old-location: directdraw\idirectdrawclipper_iscliplistchanged.htm
tech.root: directdraw
ms.assetid: d394b638-6015-47d8-89ea-2ed71611ddb3
ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],IsClipListChanged method, IDirectDrawClipper.IsClipListChanged, IDirectDrawClipper::IsClipListChanged, IsClipListChanged, IsClipListChanged method [DirectDraw], IsClipListChanged method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::IsClipListChanged, directdraw.idirectdrawclipper_iscliplistchanged
f1_keywords:
- ddraw/IDirectDrawClipper.IsClipListChanged
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
- IDirectDrawClipper.IsClipListChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the status of the clip list. This parameter is TRUE if the clip list has changed, and FALSE otherwise.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>