---
UID: NS:fwpmtypes.FWPM_SESSION0_
title: FWPM_SESSION0 (fwpmtypes.h)
description: Stores the state associated with a client session.
helpviewer_keywords: ["FWPM_SESSION0","FWPM_SESSION0 structure [Filtering]","FWPM_SESSION_FLAG_DYNAMIC","FWPM_SESSION_FLAG_RESERVED","fwp.fwpm_session0_struct","fwpmtypes/FWPM_SESSION0"]
old-location: fwp\fwpm_session0_struct.htm
tech.root: fwp
ms.assetid: 9f259ab7-cec9-44c1-8914-2850235470b3
ms.date: 12/05/2018
ms.keywords: FWPM_SESSION0, FWPM_SESSION0 structure [Filtering], FWPM_SESSION_FLAG_DYNAMIC, FWPM_SESSION_FLAG_RESERVED, fwp.fwpm_session0_struct, fwpmtypes/FWPM_SESSION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_SESSION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SESSION0_
 - fwpmtypes/FWPM_SESSION0_
 - FWPM_SESSION0
 - fwpmtypes/FWPM_SESSION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SESSION0
---

# FWPM_SESSION0 structure


## -description

The <b>FWPM_SESSION0</b> structure stores the state associated with a client session.

## -struct-fields

### -field sessionKey

Uniquely identifies the session. 

If this member is zero in the
   call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a>, Base Filtering Engine (BFE) will generate a GUID.

### -field displayData

Allows sessions to be annotated in a human-readable form.

See [FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0) for more information.

### -field flags

Settings to control session behavior.

<table>
<tr>
<th>Session flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_SESSION_FLAG_DYNAMIC"></a><a id="fwpm_session_flag_dynamic"></a><dl>
<dt><b>FWPM_SESSION_FLAG_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, any objects added during the session are
automatically deleted when the session ends.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_SESSION_FLAG_RESERVED"></a><a id="fwpm_session_flag_reserved"></a><dl>
<dt><b>FWPM_SESSION_FLAG_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>

### -field txnWaitTimeoutInMSec

Time in milli-seconds that a client will wait to begin a transaction. 

If this member is zero, BFE will use a
   default timeout.

### -field processId

Process ID of the client.

### -field sid

SID of the client.

### -field username

User name of the client.

### -field kernelMode

TRUE if this is a kernel-mode client.

## -remarks

This structure contains information supplied by the client when creating a session by calling <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a>, or information retrieved from the system when enumerating sessions by calling <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsessionenum0">FwpmSessionEnum0</a>.

The members <b>processId</b>, <b>sid</b>,  <b>username</b>, and <b>kernelMode</b> are not supplied by the client. They are supplied by BFE and can be retrieved when enumerating sessions.

<b>FWPM_SESSION0</b> is a specific implementation of FWPM_SESSION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_DISPLAY_DATA0](/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsessionenum0">FwpmSessionEnum0</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>