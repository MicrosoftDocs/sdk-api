---
UID: NE:dxcore_interface.DXCoreAdapterState
title: DXCoreAdapterState
description: Defines constants that specify kinds of DXCore adapter states.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/11/2019
ms.keywords: DXCoreAdapterState enumeration, dxcore_interface.dxcoreadapterstate
ms.localizationpriority: low
ms.topic: reference
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
 - DXCoreAdapterState
---

## -description

Defines constants that specify kinds of DXCore adapter states. Pass one of these constants to the [IDXCoreAdapter::QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate) method to set an adapter's info for a state item.

## -enum-fields

### -field IsDriverUpdateInProgress:0

Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed. If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.

When calling [QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.

<b>Important</b>. This state item is not supported for [SetState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate).

### -field AdapterMemoryBudget:1

Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.

When calling [QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.

<b>Important</b>. This state item is not supported for [SetState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate).

### -field AdapterMemoryReservation

Specifies the <em>AdapterMemoryReservation</em> adapter state, which represents the minimum required physical memory to set, in bytes, on the adapter. We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without. This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.

When calling [SetState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate), the <em>AdapterMemoryReservation</em> adapter state has type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.

<b>Important</b>. This state item is not supported for [QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate).

## -see-also

[IDXCoreAdapter::QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), [IDXCoreAdapter::SetState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
