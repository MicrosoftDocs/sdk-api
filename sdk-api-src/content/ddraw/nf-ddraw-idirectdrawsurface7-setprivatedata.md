---
UID: NF:ddraw.IDirectDrawSurface7.SetPrivateData
title: IDirectDrawSurface7::SetPrivateData (ddraw.h)
description: Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.
helpviewer_keywords: ["(none)","DDSPD_IUNKNOWNPOINTER","DDSPD_VOLATILE","IDirectDrawSurface7 interface [DirectDraw]","SetPrivateData method","IDirectDrawSurface7.SetPrivateData","IDirectDrawSurface7::SetPrivateData","SetPrivateData","SetPrivateData method [DirectDraw]","SetPrivateData method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetPrivateData","directdraw.idirectdrawsurface7_setprivatedata"]
old-location: directdraw\idirectdrawsurface7_setprivatedata.htm
tech.root: directdraw
ms.assetid: 822e4533-9073-4590-844e-8830110e4e33
ms.date: 12/05/2018
ms.keywords: (none), DDSPD_IUNKNOWNPOINTER, DDSPD_VOLATILE, IDirectDrawSurface7 interface [DirectDraw],SetPrivateData method, IDirectDrawSurface7.SetPrivateData, IDirectDrawSurface7::SetPrivateData, SetPrivateData, SetPrivateData method [DirectDraw], SetPrivateData method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetPrivateData, directdraw.idirectdrawsurface7_setprivatedata
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
 - IDirectDrawSurface7::SetPrivateData
 - ddraw/IDirectDrawSurface7::SetPrivateData
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
 - IDirectDrawSurface7.SetPrivateData
---

# IDirectDrawSurface7::SetPrivateData


## -description

Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.

## -parameters

### -param unnamedParam1 [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be set.

### -param unnamedParam2 [in]

A pointer to a buffer that contains the data to be associated with the surface.

### -param unnamedParam3 [in]

The size value of the buffer at <i>lpData</i>, in bytes.

### -param unnamedParam4 [in]

A value that can be set to one of the following flags. These flags describe the type of data being passed or request that the data be invalidated when the surface changes.



#### (none)

If no flags are specified, DirectDraw allocates memory to hold the data within the buffer and copies the data into the new buffer. The buffer allocated by DirectDraw is automatically freed, as appropriate.



#### DDSPD_IUNKNOWNPOINTER

The data at <i>lpData</i> is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. DirectDraw automatically calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> method of this interface. When this data is no longer needed, DirectDraw automatically calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method of this interface.



#### DDSPD_VOLATILE

The buffer at <i>lpData</i> is only valid while the surface remains unchanged. If the surface's contents change, subsequent calls to the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getprivatedata">IDirectDrawSurface7::GetPrivateData</a> method return DDERR_EXPIRED.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

DirectDraw does not manage the memory at <i>lpData</i>. If this buffer was dynamically allocated, the caller must free the memory.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>