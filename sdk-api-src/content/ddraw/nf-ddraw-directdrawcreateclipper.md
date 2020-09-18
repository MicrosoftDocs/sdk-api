---
UID: NF:ddraw.DirectDrawCreateClipper
title: DirectDrawCreateClipper function (ddraw.h)
description: Creates an instance of a DirectDrawClipper object that is not associated with a DirectDraw object.
helpviewer_keywords: ["DirectDrawCreateClipper","DirectDrawCreateClipper function [DirectDraw]","ddraw/DirectDrawCreateClipper","directdraw.directdrawcreateclipper"]
old-location: directdraw\directdrawcreateclipper.htm
tech.root: directdraw
ms.assetid: 12d499d2-dd4a-4831-9290-c225aec1a160
ms.date: 12/05/2018
ms.keywords: DirectDrawCreateClipper, DirectDrawCreateClipper function [DirectDraw], ddraw/DirectDrawCreateClipper, directdraw.directdrawcreateclipper
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
 - DirectDrawCreateClipper
 - ddraw/DirectDrawCreateClipper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddraw.dll
api_name:
 - DirectDrawCreateClipper
---

# DirectDrawCreateClipper function


## -description

Creates an instance of a DirectDrawClipper object that is not associated with a DirectDraw object.

## -parameters

### -param dwFlags [in]

Currently not used and must be set to 0.

### -param lplpDDClipper [out]

Address of a pointer to be filled with the address of the new DirectDrawClipper object.

### -param pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Currently, this function returns an error if this parameter is not NULL.

## -returns

If the function succeeds, the return value is DD_OK.



If it fails, the function can return one of the following error values:

<ul>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

You can call <b>DirectDrawCreateClipper</b> before any DirectDraw objects are created. Because these DirectDrawClipper objects are not owned by any DirectDraw object, they are not automatically released when an application's objects are released. If the application does not explicitly release the DirectDrawClipper objects, DirectDraw releases them when the application terminates.

To create a DirectDrawClipper object that is owned by a specific DirectDraw object, use the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createclipper">IDirectDraw7::CreateClipper</a> method.



You must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>DirectDrawCreateClipper</b> function.