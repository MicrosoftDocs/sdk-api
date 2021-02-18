---
UID: NS:winnt._PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
tech.root: 
title: PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
ms.date: 02/02/2021
ms.topic: language-reference
targetos: Windows
description: Contains dynamic enforced address ranges used by various features related to user-mode Hardware-enforced Stack Protection (HSP).
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041.662)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041.662)
req.target-type: 
req.typenames: PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE, *PPROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - PPROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
f1_keywords:
 - _PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - winnt/_PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - PPROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - winnt/PPROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
 - winnt/PROCESS_DYNAMIC_ENFORCED_ADDRESS_RANGE
dev_langs:
 - c++
---

## -description

> [!NOTE]
> This API was added to the 19041 SDK in an update released in November 2020.

Contains dynamic enforced address ranges used by various features related to user-mode Hardware-enforced Stack Protection (HSP). The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessdynamicenforcedcetcompatibleranges">SetProcessDynamicEnforcedCetCompatibleRanges</a> function uses this structure.

## -struct-fields

### -field BaseAddress

The base address of a dynamic enforced address range.

### -field Size

The size in bytes of a dynamic enforced address range.

### -field Flags

Flags that apply to the dynamic enforced address range described by <i>BaseAddress</i> and <i>Size</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DYNAMIC_ENFORCED_ADDRESS_RANGE_ADD"></a><a id="dynamic_enforced_address_range_add"></a><dl>
<dt><b>DYNAMIC_ENFORCED_ADDRESS_RANGE_ADD</b></dt>
<dt>0x00000001UL</dt>
</dl>
</td>
<td width="60%">
Dynamic enforced address range should be added. If this flag is not set, the range is removed. This is an input flag.

</td>
</tr>
<tr>
<td width="40%"><a id="DYNAMIC_ENFORCED_ADDRESS_RANGE_PROCESSED"></a><a id="dynamic_enforced_address_range_processed"></a><dl>
<dt><b>DYNAMIC_ENFORCED_ADDRESS_RANGE_PROCESSED</b></dt>
<dt>0x00000002UL</dt>
</dl>
</td>
<td width="60%">
Dynamic enforced address range has been successfully processed (either added or removed).
This is an output flag used to report which ranges were successfully processed when processing an array of multiple ranges.

</td>
</tr>
</table>

## -remarks

## -see-also

