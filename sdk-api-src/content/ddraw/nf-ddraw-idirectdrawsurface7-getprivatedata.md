---
UID: NF:ddraw.IDirectDrawSurface7.GetPrivateData
title: IDirectDrawSurface7::GetPrivateData (ddraw.h)
description: Copies the private data that is associated with this surface to a provided buffer.
helpviewer_keywords: ["GetPrivateData","GetPrivateData method [DirectDraw]","GetPrivateData method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetPrivateData method","IDirectDrawSurface7.GetPrivateData","IDirectDrawSurface7::GetPrivateData","ddraw/IDirectDrawSurface7::GetPrivateData","directdraw.idirectdrawsurface7_getprivatedata"]
old-location: directdraw\idirectdrawsurface7_getprivatedata.htm
tech.root: directdraw
ms.assetid: f8c0c882-329f-4cce-8cd0-ff71c18b1716
ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method [DirectDraw], GetPrivateData method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPrivateData method, IDirectDrawSurface7.GetPrivateData, IDirectDrawSurface7::GetPrivateData, ddraw/IDirectDrawSurface7::GetPrivateData, directdraw.idirectdrawsurface7_getprivatedata
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
 - IDirectDrawSurface7::GetPrivateData
 - ddraw/IDirectDrawSurface7::GetPrivateData
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
 - IDirectDrawSurface7.GetPrivateData
---

# IDirectDrawSurface7::GetPrivateData


## -description

Copies the private data that is associated with this surface to a provided buffer.

## -parameters

### -param unnamedParam1 [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be retrieved.

### -param unnamedParam2 [out]

A pointer to a previously allocated buffer that receives the requested private data if the call succeeds. The application that calls this method must allocate and release this buffer.

### -param unnamedParam3 [in, out]

A pointer to a variable that contains the size value of the buffer at <i>lpBuffer</i>, in bytes. If this value is less than the actual size of the private data (such as 0), <b>GetPrivateData</b> sets the variable to the required buffer size, and then returns DDERR_MOREDATA.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXPIRED</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_MOREDATA</li>
<li>DDERR_NOTFOUND</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

If the data returned is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or one of its derivative classes, which was previously set by **SetPrivateData** with a `DDSPD_IUNKNOWNPOINTER` flag, that interface will have its reference count incremented before the private data is returned.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>