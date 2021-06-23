---
UID: NF:presentation.IPresentationSurface.RestrictToOutput
tech.root: composition_presentation
title: IPresentationSurface::RestrictToOutput
ms.date: 06/08/2021
targetos: Windows
description: Restricts presentation to a specific display adapter output.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - presentation.h
api_name:
 - IPresentationSurface::RestrictToOutput
f1_keywords:
 - IPresentationSurface::RestrictToOutput
 - presentation/IPresentationSurface::RestrictToOutput
dev_langs:
 - c++
---

## -description

Restricts presentation to a specific display adapter output.

## -parameters

### -param output

Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

An object that represents the adapter output. Only an [IDXGIOutput](/windows/win32/api/dxgi/nn-dxgi-idxgioutput) is accepted.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

