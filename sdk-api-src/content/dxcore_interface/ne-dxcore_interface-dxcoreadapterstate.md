---
UID: NE:dxcore_interface.DXCoreAdapterState
title: DXCoreAdapterState
description: Defines constants that specify kinds of DXCore adapter states.
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 09/16/2024
ms.keywords: DXCoreAdapterState enumeration, dxcore_interface.dxcoreadapterstate
ms.localizationpriority: low
ms.topic: reference
targetos: Windows
ms.service: windows
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
prerelease: true
---

## -description

Defines constants that specify kinds of DXCore adapter states. Pass one of these constants to the [IDXCoreAdapter::QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate) method to set an adapter's info for a state item.

## -enum-fields

### -field IsDriverUpdateInProgress:0

Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed. If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.

When calling [QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.

<b>Important</b>. This state item is not supported for [SetState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate).

### -field AdapterMemoryBudget:1

Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.

When calling [QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/api/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.

<b>Important</b>. This state item is not supported for [SetState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate).

### -field AdapterMemoryUsageBytes:2

This query takes Physical Adapter Index and Dedicated vs. Shared as input; and outputs the Committed and Resident Memory Dedicated or Shared portions of GPU Memory, respectively.

### -field AdapterMemoryUsageByProcessBytes:3

This query takes Engine ID, Physical Adapter Index, and Process Handle as input; and outputs Committed Memory and Resident Memory on Dedicated or Shared portions of GPU Memory, respectively.

### -field AdapterEngineRunningTimeMicroseconds:4

This query takes Engine ID and Physical Adapter Index as input; and outputs Engine Running Time as output.

### -field AdapterEngineRunningTimeByProcessMicroseconds:5

This query takes Engine ID, Physical Adapter Index, and Process Handle as input; and outputs Engine Running Time as output.

### -field AdapterTemperatureCelsius:6

This query takes Physical Adapter Index as input, and outputs Current GPU Temperature in Degrees Celsius.

### -field AdapterInUseProcessCount:7

This returns the number of processes using this adapter, and the PIDs in it, respectively.

### -field AdapterInUseProcessSet:8

This returns the number of processes using this adapter, and the PIDs in it, respectively.

### -field AdapterEngineFrequencyHertz:9

This query takes in the physical adapter and engine indices, and outputs the clock frequency of the respective engine in hertz. The output structure also includes the maximum frequency for the engine, with and without overclocking.

<pre><code class="lang-cppwinrt">
uint64_t GetEngineFrequency(com_ptr<IDXCoreAdapter1> adapter, uint32_t physicalIndex, uint32_t engineIndex)
{
    DXCoreAdapterEngineIndex index;
    index.PhysicalAdapterIndex = physicalIndex;
    index.EngineIndex = engineIndex;

    DXCoreFrequencyQueryOutput frequencyData = {};

    winrt::check_hresult(adapter->QueryState(DXCoreAdapterState::AdapterEngineFrequencyHertz, &index, &frequencyData));

    return frequencyData.Frequency;
}
</code></pre>

### -field AdapterMemoryFrequencyHertz:10

This query takes in the physical adapter index, and outputs the clock frequency of its memory in hertz. The output structure also includes the maximum frequency for the memory, with and without overclocking.

<pre><code class="lang-cppwinrt">
uint64_t GetEngineFrequency(com_ptr<IDXCoreAdapter1> adapter, uint32_t physicalIndex, uint32_t engineIndex)
{
uint64_t GetMemoryFrequency(com_ptr<IDXCoreAdapter1> adapter, uint32_t physicalIndex)
{
    DXCoreFrequencyQueryOutput frequencyData = {};

    winrt::check_hresult(adapter->QueryState(DXCoreAdapterState::AdapterMemoryFrequencyHertz, &physicalIndex, &frequencyData));

    return frequencyData.frequency;
}
</code></pre>

## -see-also

[IDXCoreAdapter::QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate), [IDXCoreAdapter::SetState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate), [DXCore reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
