---
UID: NF:windows.devices.display.core.interop.IDisplayPathInterop.GetSourceId
title: IDisplayPathInterop::GetSourceId
description: TBD
helpviewer_keywords: ["IDisplayPathInterop::GetSourceId"]
ms.date: 02/10/2020
tech.root: winrt
dev_langs:
- c++
req.header: windows.devices.display.core.interop.h
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
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12.dll
api_name:
 - IDisplayPathInterop::GetSourceId
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Gets the unique identifier of the [DisplaySource](/uwp/api/windows.devices.display.core.displaysource) object.

## -parameters

### -param pSourceId [out]

The unique identifier.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

This method returns **S_OK** if it succeeded, otherwise a failure code indicating why it failed. 

## -remarks

## -see-also
