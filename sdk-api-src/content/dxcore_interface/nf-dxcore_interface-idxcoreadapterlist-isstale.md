---
UID: NF:dxcore_interface.IDXCoreAdapterList.IsStale
title: IDXCoreAdapterList::IsStale
description: Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,IsStale method, IDXCoreAdapterFactory.IsStale, IDXCoreAdapterFactory::IsStale, IsStale, IsStale method, IsStale method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::IsStale, dxcore_interface.idxcoreadapterfactory_isstale
ms.localizationpriority: low
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: method
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
 - COM
api_location:
 - dxcore.dll
api_name:
 - IDXCoreAdapterList::IsStale
---

## -description

Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).



## -returns

Type: **bool**

Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale. Otherwise, returns `false`.

## -remarks

You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date. If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object. A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).

## -see-also

[IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
