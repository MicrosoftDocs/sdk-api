---
UID: NF:presentation.IPresentationSurface.SetTransform
tech.root: directcomp
title: IPresentationSurface::SetTransform
ms.date: 06/08/2021
targetos: Windows
description: Sets the transform applied to the source buffer area to define the on-screen area where the buffer will appear.
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
 - IPresentationSurface::SetTransform
f1_keywords:
 - IPresentationSurface::SetTransform
 - presentation/IPresentationSurface::SetTransform
dev_langs:
 - c++
---

## -description

Sets the transform applied to the source buffer area to define the on-screen area where the buffer will appear.

## -parameters

### -param transform

Type: **[PresentationTransform](../presentationtypes/ns-presentationtypes-presentationtransform.md)**

A transform applied to the source buffer area to define the on-screen area where the buffer will appear.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

