---
UID: NF:tbs.Tbsi_Revoke_Attestation
title: Tbsi_Revoke_Attestation function (tbs.h)
description: Invalidates the PCRs if the ELAM driver detects a policy-violation (a rootkit, for example).
helpviewer_keywords: ["Tbsi_Revoke_Attestation","Tbsi_Revoke_Attestation function [TBS]","tbs.tbsi_revoke_attestation","tbs/Tbsi_Revoke_Attestation"]
old-location: tbs\tbsi_revoke_attestation.htm
tech.root: TBS
ms.assetid: 64B6BC8F-5031-4A31-86FD-DECA6203D6E4
ms.date: 12/05/2018
ms.keywords: Tbsi_Revoke_Attestation, Tbsi_Revoke_Attestation function [TBS], tbs.tbsi_revoke_attestation, tbs/Tbsi_Revoke_Attestation
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsi_Revoke_Attestation
 - tbs/Tbsi_Revoke_Attestation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsi_Revoke_Attestation
---

# Tbsi_Revoke_Attestation function


## -description

Invalidates the PCRs if the ELAM driver detects a policy-violation (a rootkit, for example).



## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INTERNAL_ERROR</b></dt>
<dt>2150121473 (0x80284001)</dt>
</dl>
</td>
<td width="60%">
An internal software error occurred. 

<div class="alert"><b>Note</b>  If TBS_E_INTERNAL_ERROR is returned, the system event log may contain event ID 16385 from the TBS event source with error code 0x80070032.  This may indicate that the hardware platform does not provide a TCG event log to the operating system.  Sometimes this can be resolved by installing a BIOS upgrade from the platform manufacturer.</div>
<div> </div>
</td>
</tr>
</table>

## -remarks

This function is callable from kernel mode.

You must run this function with administrative rights. This function extends PCR[12] by an unspecified value and increment the event counter in the TPM. Both actions are necessary, so the trust is broken in all quotes that are created from here on forward. Since the PCRs are reset on hibernation and the extend to PCR[12] then will disappear, a gap in the event counter will indicate a broken chain of logs.

As a result, the WBCL files will not reflect the current state of the TPM for the remainder of the time that the TPM is powered up and remote systems will not be able to form trust in the security state of the system.  Note that anti-malware systems will probably perform additional remediation or alerts, but the invalidation step is crucial if attestation is supported.

When the computer goes to hibernation and subsequently resumes, the previous PCR extent will be lost, and the broken trust will not be reflected in the PCR measurements anymore. To address this, the <b>Tbsi_Revoke_Attestation</b> function also increments the monotonic Event Counter located in the TPM. Further TPM attestation validations will notice a gap in the archived WBCL logs’ boot counter values. Upon discovery of such a gap, attestation validation code should fail the validation, just as it would if other required events were not present in the log. Note that the counter in the TPM cannot be rolled back you can't construct the missing WBCL after the fact.

