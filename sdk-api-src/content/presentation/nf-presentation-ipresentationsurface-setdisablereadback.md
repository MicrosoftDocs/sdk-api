---
UID: NF:presentation.IPresentationSurface.SetDisableReadback
tech.root: comp_swapchain
title: IPresentationSurface::SetDisableReadback
ms.date: 06/08/2021
targetos: Windows
description: Sets a flag to disable or enable buffer read back.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dcomp.dll
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dcomp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - IPresentationSurface::SetDisableReadback
f1_keywords:
 - IPresentationSurface::SetDisableReadback
 - presentation/IPresentationSurface::SetDisableReadback
dev_langs:
 - c++
---

## -description

Sets a flag to disable or enable buffer read back.

## -parameters

### -param value

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` if read back is disabled; otherwise, `FALSE`.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

Pass `TRUE` to this function to prevent the compositor from ever rendering the buffer into a form of capture (screen capture, window capture, etc.)

## -see-also

