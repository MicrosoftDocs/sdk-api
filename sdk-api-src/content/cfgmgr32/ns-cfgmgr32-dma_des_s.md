---
UID: NS:cfgmgr32.DMA_Des_s
title: DMA_Des_s
author: windows-sdk-content
description: The DMA_DES structure is used for specifying either a resource list or a resource requirements list that describes direct memory access (DMA) channel usage for a device instance.
old-location: devinst\dma_des.htm
old-project: devinst
ms.assetid: e357132d-ba40-4c14-813c-505aadc94a26
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*PDMA_DES, DMA_DES, DMA_DES structure [Device and Driver Installation], DMA_Des_s, PDMA_DES, PDMA_DES structure pointer [Device and Driver Installation], cfgmgr32/DMA_DES, cfgmgr32/PDMA_DES, cfgmgrst_342a3feb-d7c8-46bb-8672-009f024374d7.xml, devinst.dma_des"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
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
tech.root: 
req.typenames: DMA_DES, *PDMA_DES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - DMA_DES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DMA_Des_s structure


## -description


The DMA_DES structure is used for specifying either a resource list or a resource requirements list that describes direct memory access (DMA) channel usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field DD_Count





#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544762">DMA_RANGE</a> array that is included in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544764">DMA_RESOURCE</a> structure.


### -field DD_Type

Must be set to the constant value <b>DType_Range</b>.


### -field DD_Flags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>Channel Width Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_BYTE</b>

</td>
<td>
8-bit DMA channel.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_WORD</b>

</td>
<td>
16-bit DMA channel.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_DWORD</b>

</td>
<td>
32-bit DMA channel.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_BYTE_AND_WORD</b>

</td>
<td>
8-bit and 16-bit DMA channel.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mDD_Width</b>

</td>
<td>
Bitmask for the bits within <b>DD_Flags</b> that specify the channel width value.

</td>
</tr>
<tr>
<td colspan="2">
<i>Bus Mastering Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_NoBusMaster</b>

</td>
<td>
No bus mastering.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_BusMaster</b>

</td>
<td>
Bus mastering.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mDD_BusMaster</b>

</td>
<td>
Bitmask for the bits within <b>DD_Flags</b> that specify the bus mastering value.

</td>
</tr>
<tr>
<td colspan="2">
<i>DMA Type Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_TypeStandard</b>

</td>
<td>
Standard DMA.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_TypeA</b>

</td>
<td>
Type A DMA.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_TypeB</b>

</td>
<td>
Type B DMA.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fDD_TypeF</b>

</td>
<td>
Type F DMA.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mDD_Type</b>

</td>
<td>
Bitmask for the bits within <b>DD_Flags</b> that specify the DMA type value.

</td>
</tr>
</table>
 


### -field DD_Alloc_Chan





#### For a resource list:

The DMA channel allocated to the device.



#### For a resource requirements list:

<i>Not used.</i>


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544762">DMA_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544764">DMA_RESOURCE</a>
 

 

