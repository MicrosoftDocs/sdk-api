---
UID: NS:winnt._PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
title: PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
ms.date: 4/28/2020
targetos: Windows
description: Contains dynamic exception handling continuation targets.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: PROCESS_DYNAMIC_EH_CONTINUATION_TARGET, *PPROCESS_DYNAMIC_EH_CONTINUATION_TARGET
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
f1_keywords:
 - _PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - winnt/_PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - PPROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - winnt/PPROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
 - winnt/PROCESS_DYNAMIC_EH_CONTINUATION_TARGET
dev_langs:
 - c++
---

## -description

Contains dynamic exception handling continuation targets. The <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessdynamicehcontinuationtargets">SetProcessDynamicEHContinuationTargets</a> function uses this structure.

## -struct-fields

### -field TargetAddress

The address of a dynamic exception handling continuation target.

### -field Flags

Flags that apply to the dynamic exception handling continuation target in <i>TargetAddress</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DYNAMIC_EH_CONTINUATION_TARGET_ADD"></a><a id="dynamic_eh_continuation_target_add"></a><dl>
<dt><b>DYNAMIC_EH_CONTINUATION_TARGET_ADD</b></dt>
<dt>0x00000001UL</dt>
</dl>
</td>
<td width="60%">
Dynamic exception handling continuation target should be added. If this flag is not set, the target is removed. This is an input flag.

</td>
</tr>
<tr>
<td width="40%"><a id="DYNAMIC_EH_CONTINUATION_TARGET_PROCESSED"></a><a id="dynamic_eh_continuation_target_processed"></a><dl>
<dt><b>DYNAMIC_EH_CONTINUATION_TARGET_PROCESSED</b></dt>
<dt>0x00000002UL</dt>
</dl>
</td>
<td width="60%">
Dynamic exception handling continuation target has been successfully processed (either added or removed).
This is an output flag used to report which targets were successfully processed when processing an array of multiple targets.

</td>
</tr>
</table>

## -remarks

## -see-also

