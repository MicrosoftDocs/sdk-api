---
UID: NF:ddraw.IDirectDrawClipper.GetClipList
title: IDirectDrawClipper::GetClipList (ddraw.h)
description: Retrieves a copy of the clip list that is associated with a DirectDrawClipper object. To select a subset of the clip list, you can pass a rectangle that clips the clip list.
helpviewer_keywords: ["GetClipList","GetClipList method [DirectDraw]","GetClipList method [DirectDraw]","IDirectDrawClipper interface","IDirectDrawClipper interface [DirectDraw]","GetClipList method","IDirectDrawClipper.GetClipList","IDirectDrawClipper::GetClipList","ddraw/IDirectDrawClipper::GetClipList","directdraw.idirectdrawclipper_getcliplist"]
old-location: directdraw\idirectdrawclipper_getcliplist.htm
tech.root: directdraw
ms.assetid: 0446f8b9-c965-4336-ae78-5bb791861844
ms.date: 12/05/2018
ms.keywords: GetClipList, GetClipList method [DirectDraw], GetClipList method [DirectDraw],IDirectDrawClipper interface, IDirectDrawClipper interface [DirectDraw],GetClipList method, IDirectDrawClipper.GetClipList, IDirectDrawClipper::GetClipList, ddraw/IDirectDrawClipper::GetClipList, directdraw.idirectdrawclipper_getcliplist
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
 - IDirectDrawClipper::GetClipList
 - ddraw/IDirectDrawClipper::GetClipList
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
 - IDirectDrawClipper.GetClipList
---

# IDirectDrawClipper::GetClipList


## -description

Retrieves a copy of the clip list that is associated with a DirectDrawClipper object. To select a subset of the clip list, you can pass a rectangle that clips the clip list.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that <b>GetClipList</b> uses to clip the clip list. Set this parameter to NULL to retrieve the entire clip list.

### -param unnamedParam2 [out]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure that receives the resulting copy of the clip list. If this parameter is NULL, <b>GetClipList</b> fills the variable at <i>lpdwSize</i> with the number of bytes necessary to hold the entire clip list.

### -param unnamedParam3 [out]

A pointer to a variable that receives the size of the resulting clip list. When retrieving the clip list, this parameter is the size of the buffer at <i>lpClipList</i>. When <i>lpClipList</i> is NULL, the variable at <i>lpdwSize</i> receives the required size of the buffer, in bytes.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCLIPLIST</li>
<li>DDERR_REGIONTOOSMALL</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a>