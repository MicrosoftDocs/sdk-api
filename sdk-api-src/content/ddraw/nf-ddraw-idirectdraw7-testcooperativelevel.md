---
UID: NF:ddraw.IDirectDraw7.TestCooperativeLevel
title: IDirectDraw7::TestCooperativeLevel (ddraw.h)
description: Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.
helpviewer_keywords: ["IDirectDraw7 interface [DirectDraw]","TestCooperativeLevel method","IDirectDraw7.TestCooperativeLevel","IDirectDraw7::TestCooperativeLevel","TestCooperativeLevel","TestCooperativeLevel method [DirectDraw]","TestCooperativeLevel method [DirectDraw]","IDirectDraw7 interface","ddraw/IDirectDraw7::TestCooperativeLevel","directdraw.idirectdraw7_testcooperativelevel"]
old-location: directdraw\idirectdraw7_testcooperativelevel.htm
tech.root: directdraw
ms.assetid: 6bbabd8c-f48e-480c-9ea4-06e4fce1255a
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],TestCooperativeLevel method, IDirectDraw7.TestCooperativeLevel, IDirectDraw7::TestCooperativeLevel, TestCooperativeLevel, TestCooperativeLevel method [DirectDraw], TestCooperativeLevel method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::TestCooperativeLevel, directdraw.idirectdraw7_testcooperativelevel
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
 - IDirectDraw7::TestCooperativeLevel
 - ddraw/IDirectDraw7::TestCooperativeLevel
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
 - IDirectDraw7.TestCooperativeLevel
---

# IDirectDraw7::TestCooperativeLevel


## -description

Reports the current cooperative-level status of the DirectDraw device for a windowed or full-screen application.



## -returns

If the method succeeds, the return value is DD_OK, which indicates that the calling application can continue.

If it fails, the method can return one of the following error values (see Remarks):

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_EXCLUSIVEMODEALREADYSET</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_WRONGMODE</li>
</ul>

## -remarks

This method is particularly useful to applications that use the WM_ACTIVATEAPP and WM_DISPLAYCHANGE system messages as a notification to restore surfaces or recreate DirectDraw objects. The DD_OK return value always indicates that the application can continue, but the error codes are interpreted differently, depending on the cooperative level that the application uses.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
