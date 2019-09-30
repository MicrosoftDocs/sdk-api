---
UID: NF:windows.graphics.capture.interop.IGraphicsCaptureItemInterop.CreateForMonitor
title: IGraphicsCaptureItemInterop::CreateForMonitor
description: Targets a monitor(s) for the creation of a graphics capture item.
ms.date: 6/24/2019
ms.keywords: IGraphicsCaptureItemInterop::CreateForMonitor
ms.topic: language-reference
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.graphics.capture.interop.h
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
 - windows.h
api_name:
 - IGraphicsCaptureItemInterop::CreateForMonitor
tech.root: winrt
---

## -description

Targets a monitor(s) for the creation of a graphics capture item.

## -parameters

### -param monitor

Type: **HMONITOR**

The monitor handle that represents the monitor to capture.

### -param riid

Type: **REFIID**

GUID for the type returned. Supported value: [GraphicsCaptureItem](https://docs.microsoft.com/uwp/api/windows.graphics.capture.graphicscaptureitem).

### -param result

Type: **void\*\***

Out pointer for the object to receive.

## -returns

Type: **HRESULT**

The return error code.

## -remarks

## -see-also
