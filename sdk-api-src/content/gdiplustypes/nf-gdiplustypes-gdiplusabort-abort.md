---
UID: NF:gdiplustypes.GdiplusAbort.Abort
title: GdiplusAbort::Abort
ms.date: 11/4/2019
ms.topic: language-reference
tech.root: gdiplus
targetos: Windows
description: \**Abort** is an application-defined method that is called periodically by Windows GDI+ during time-consuming rendering operations. See the [**GdiplusAbort**](ns-gdiplustypes-gdiplusabort) structure.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplustypes.h
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
 - gdiplustypes.h
api_name:
 - GdiplusAbort::Abort
f1_keywords:
 - GdiplusAbort::Abort
 - gdiplustypes/GdiplusAbort::Abort
dev_langs:
 - c++
---

## -description

**Abort** is an application-defined method that is called periodically by Windows GDI+ during time-consuming rendering operations. See the [**GdiplusAbort**](ns-gdiplustypes-gdiplusabort) structure.

## -parameters

### -param arg1

Type: **[VOID](/windows/win32/winprog/windows-data-types)**

**Abort** doesn't take any parameters.

## -returns

Return **S_OK** for GDI+ to continue the rendering operation. Return **E_ABORT** for GDI+ to abort the rendering operation.

## -remarks

## -see-also

[GdiplusAbort](ns-gdiplustypes-gdiplusabort)

