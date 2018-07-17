---
UID: NS:cfgmgr32.Mem_Range_s
title: Mem_Range_s
author: windows-sdk-content
description: The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
old-location: devinst\mem_range.htm
old-project: devinst
ms.assetid: a31ae199-8f4a-4d1f-891c-f1dc11a4edde
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: "*PMEM_RANGE, MEM_RANGE, MEM_RANGE structure [Device and Driver Installation], Mem_Range_s, PMEM_RANGE, PMEM_RANGE structure pointer [Device and Driver Installation], cfgmgr32/MEM_RANGE, cfgmgr32/PMEM_RANGE, cfgmgrst_f2ac1f4b-c29b-41fd-bacb-e7a8f4bc6f45.xml, devinst.mem_range"
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
req.typenames: MEM_RANGE, *PMEM_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - MEM_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Mem_Range_s structure


## -description


The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance. For more information about resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field MR_Align

Mask used to specify the memory address boundary on which the first allocated memory address must be aligned.


### -field MR_nBytes

The number of bytes of memory required by the device.


### -field MR_Min

The lowest-numbered of a range of contiguous memory addresses that can be allocated to the device.


### -field MR_Max

The highest-numbered of a range of contiguous memory addresses that can be allocated to the device.


### -field MR_Flags

One bit flag from <i>each</i> of the flag sets described in the table included with the description of the <b>MD_Flags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548716">MEM_DES</a> structure.


### -field MR_Reserved

<i>For internal use only.</i>


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548716">MEM_DES</a>
 

 

