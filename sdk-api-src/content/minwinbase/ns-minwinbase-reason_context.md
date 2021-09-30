---
UID: NS:minwinbase._REASON_CONTEXT
title: REASON_CONTEXT (minwinbase.h)
description: Contains information about a power request. This structure is used by the PowerCreateRequest and SetWaitableTimerEx functions.
helpviewer_keywords: ["*PREASON_CONTEXT","POWER_REQUEST_CONTEXT_DETAILED_STRING","POWER_REQUEST_CONTEXT_SIMPLE_STRING","PREASON_CONTEXT","PREASON_CONTEXT structure pointer","REASON_CONTEXT","REASON_CONTEXT structure","base.reason_context","minwinbase/PREASON_CONTEXT","minwinbase/REASON_CONTEXT","winbase/PREASON_CONTEXT","winbase/REASON_CONTEXT"]
old-location: base\reason_context.htm
tech.root: base
ms.assetid: 006bb84f-5e51-4f6e-8a44-6b50e763c5ca
ms.date: 12/05/2018
ms.keywords: '*PREASON_CONTEXT, POWER_REQUEST_CONTEXT_DETAILED_STRING, POWER_REQUEST_CONTEXT_SIMPLE_STRING, PREASON_CONTEXT, PREASON_CONTEXT structure pointer, REASON_CONTEXT, REASON_CONTEXT structure, base.reason_context, minwinbase/PREASON_CONTEXT, minwinbase/REASON_CONTEXT, winbase/PREASON_CONTEXT, winbase/REASON_CONTEXT'
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REASON_CONTEXT, *PREASON_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _REASON_CONTEXT
 - minwinbase/_REASON_CONTEXT
 - PREASON_CONTEXT
 - minwinbase/PREASON_CONTEXT
 - REASON_CONTEXT
 - minwinbase/REASON_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MinWinBase.h
 - WinBase.h
api_name:
 - REASON_CONTEXT
---

# REASON_CONTEXT structure


## -description

Contains information about a power request. This structure is used by the 
    <a href="/windows/desktop/api/winbase/nf-winbase-powercreaterequest">PowerCreateRequest</a> and 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimerex">SetWaitableTimerEx</a> functions.

## -struct-fields

### -field Version

The version number of the structure. This parameter must be set to 
      <b>POWER_REQUEST_CONTEXT_VERSION</b>.

### -field Flags

The format of the reason for the power request. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="POWER_REQUEST_CONTEXT_DETAILED_STRING"></a><a id="power_request_context_detailed_string"></a><dl>
<dt><b>POWER_REQUEST_CONTEXT_DETAILED_STRING</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The <i>Detailed</i> structure identifies a localizable string resource that describes 
        the reason for the power request. 

</td>
</tr>
<tr>
<td width="40%"><a id="POWER_REQUEST_CONTEXT_SIMPLE_STRING"></a><a id="power_request_context_simple_string"></a><dl>
<dt><b>POWER_REQUEST_CONTEXT_SIMPLE_STRING</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <i>SimpleReasonString</i> parameter contains a simple, non-localizable string that 
        describes the reason for the power request.

</td>
</tr>
</table>

### -field Reason

A union that consists of either a <b>Detailed</b> structure or a string.

### -field Reason.Detailed

A structure that identifies a localizable string resource to describe the reason for the power 
       request.

### -field Reason.Detailed.LocalizedReasonModule

The module that contains the string resource.

### -field Reason.Detailed.LocalizedReasonId

The ID of the string resource.

### -field Reason.Detailed.ReasonStringCount

The number of strings in the <i>ReasonStrings</i> parameter.

### -field Reason.Detailed.ReasonStrings

An array of strings to be substituted in the string resource at run time.

### -field Reason.SimpleReasonString

A non-localized string that describes the reason for the power request.

## -remarks

It is safe to pass read-only strings as the <i>SimpleReasonString</i> or <i>ReasonStrings</i> because the <a href="/windows/desktop/api/winbase/nf-winbase-powercreaterequest">PowerCreateRequest</a> and <a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimerex">SetWaitableTimerEx</a> functions read from the strings and do not write to them.


## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-powercreaterequest">PowerCreateRequest</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimerex">SetWaitableTimerEx</a>
