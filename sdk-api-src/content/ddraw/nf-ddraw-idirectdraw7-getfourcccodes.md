---
UID: NF:ddraw.IDirectDraw7.GetFourCCCodes
title: IDirectDraw7::GetFourCCCodes (ddraw.h)
description: Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.
helpviewer_keywords: ["GetFourCCCodes","GetFourCCCodes method [DirectDraw]","GetFourCCCodes method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetFourCCCodes method","IDirectDraw7.GetFourCCCodes","IDirectDraw7::GetFourCCCodes","ddraw/IDirectDraw7::GetFourCCCodes","directdraw.idirectdraw7_getfourcccodes"]
old-location: directdraw\idirectdraw7_getfourcccodes.htm
tech.root: directdraw
ms.assetid: 980b1cfe-d466-42f4-865f-6ddc7a41ea94
ms.date: 12/05/2018
ms.keywords: GetFourCCCodes, GetFourCCCodes method [DirectDraw], GetFourCCCodes method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetFourCCCodes method, IDirectDraw7.GetFourCCCodes, IDirectDraw7::GetFourCCCodes, ddraw/IDirectDraw7::GetFourCCCodes, directdraw.idirectdraw7_getfourcccodes
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
 - IDirectDraw7::GetFourCCCodes
 - ddraw/IDirectDraw7::GetFourCCCodes
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
 - IDirectDraw7.GetFourCCCodes
---

# IDirectDraw7::GetFourCCCodes


## -description

Retrieves the four-character codes (FOURCC) that are supported by the DirectDraw object. This method can also retrieve the number of codes that are supported.

## -parameters

### -param unnamedParam1 [in, out]

A pointer to a variable that contains the number of entries that the array specified by <i>lpCodes</i> can hold. If the number of entries is too small to accommodate all the codes, <i>lpNumCodes</i> is set to the required number, and the array specified by <i>lpCodes</i> is filled with all that fits.

### -param unnamedParam2 [in, out]

An array of variables to be filled with FOURCCs that are supported by this DirectDraw object. If you specify NULL, <i>lpNumCodes</i> is set to the number of supported FOURCCs, and the method returns.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>