---
UID: NE:dxcore_interface.DXCoreAdapterPreference
title: DXCoreAdapterPreference
description: Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/11/2019
ms.keywords: DXCoreAdapterPreference enumeration, dxcore_interface.dxcoreadapterpreference
ms.localizationpriority: low
targetos: Windows
ms.prod: windows
req.assembly: 
req.construct-type: enumeration
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - HeaderDef
api_location:
 - dxcore.dll
api_name:
 - DXCoreAdapterPreference
---

## -description

Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria. You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort).

## -enum-fields

### -field Hardware:0

Specifies a preference for hardware adapters (as opposed to software adapters).

### -field MinimumPower:1

Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).

### -field HighPerformance:2

Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.

## -see-also

[IDXCoreAdapterList::Sort](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
