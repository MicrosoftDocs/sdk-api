---
UID: NS:ntsecpkg._SECPKG_PARAMETERS
title: SECPKG_PARAMETERS (ntsecpkg.h)
description: The SECPKG_PARAMETERS structure contains information about the computer system. This structure is used by the SpInitialize function.
helpviewer_keywords: ["*PSECPKG_EVENT_DOMAIN_CHANGE","*PSECPKG_PARAMETERS","PSECPKG_EVENT_DOMAIN_CHANGE","PSECPKG_EVENT_DOMAIN_CHANGE structure pointer [Security]","PSECPKG_PARAMETERS","PSECPKG_PARAMETERS structure pointer [Security]","SECPKG_EVENT_DOMAIN_CHANGE","SECPKG_EVENT_DOMAIN_CHANGE structure [Security]","SECPKG_PARAMETERS","SECPKG_PARAMETERS structure [Security]","SECPKG_STATE_DOMAIN_CONTROLLER","SECPKG_STATE_ENCRYPTION_PERMITTED","SECPKG_STATE_STANDALONE","SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED","SECPKG_STATE_WORKSTATION","_ssp_secpkg_parameters","ntsecpkg/PSECPKG_EVENT_DOMAIN_CHANGE","ntsecpkg/PSECPKG_PARAMETERS","ntsecpkg/SECPKG_EVENT_DOMAIN_CHANGE","ntsecpkg/SECPKG_PARAMETERS","security.secpkg_parameters"]
old-location: security\secpkg_parameters.htm
tech.root: security
ms.assetid: 2e3b7961-e2c4-4011-91b1-0ba9d35e9188
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_EVENT_DOMAIN_CHANGE, *PSECPKG_PARAMETERS, PSECPKG_EVENT_DOMAIN_CHANGE, PSECPKG_EVENT_DOMAIN_CHANGE structure pointer [Security], PSECPKG_PARAMETERS, PSECPKG_PARAMETERS structure pointer [Security], SECPKG_EVENT_DOMAIN_CHANGE, SECPKG_EVENT_DOMAIN_CHANGE structure [Security], SECPKG_PARAMETERS, SECPKG_PARAMETERS structure [Security], SECPKG_STATE_DOMAIN_CONTROLLER, SECPKG_STATE_ENCRYPTION_PERMITTED, SECPKG_STATE_STANDALONE, SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED, SECPKG_STATE_WORKSTATION, _ssp_secpkg_parameters, ntsecpkg/PSECPKG_EVENT_DOMAIN_CHANGE, ntsecpkg/PSECPKG_PARAMETERS, ntsecpkg/SECPKG_EVENT_DOMAIN_CHANGE, ntsecpkg/SECPKG_PARAMETERS, security.secpkg_parameters'
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SECPKG_PARAMETERS, *PSECPKG_PARAMETERS, SECPKG_EVENT_DOMAIN_CHANGE, *PSECPKG_EVENT_DOMAIN_CHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_PARAMETERS
 - ntsecpkg/_SECPKG_PARAMETERS
 - PSECPKG_PARAMETERS
 - ntsecpkg/PSECPKG_PARAMETERS
 - SECPKG_PARAMETERS
 - ntsecpkg/SECPKG_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_PARAMETERS
---

# SECPKG_PARAMETERS structure


## -description

The <b>SECPKG_PARAMETERS</b> structure contains information about the computer system. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -struct-fields

### -field Version

The version of the Security Support Provider Interface in use.

### -field MachineState

The state of the machine. The following table lists the valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_ENCRYPTION_PERMITTED"></a><a id="secpkg_state_encryption_permitted"></a><dl>
<dt><b>SECPKG_STATE_ENCRYPTION_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/s-gly">security package</a> may use encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED"></a><a id="secpkg_state_strong_encryption_permitted"></a><dl>
<dt><b>SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The security package may use strong encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_DOMAIN_CONTROLLER"></a><a id="secpkg_state_domain_controller"></a><dl>
<dt><b>SECPKG_STATE_DOMAIN_CONTROLLER</b></dt>
</dl>
</td>
<td width="60%">
The machine is a domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_WORKSTATION"></a><a id="secpkg_state_workstation"></a><dl>
<dt><b>SECPKG_STATE_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The machine is a workstation with access to a network.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_STANDALONE"></a><a id="secpkg_state_standalone"></a><dl>
<dt><b>SECPKG_STATE_STANDALONE</b></dt>
</dl>
</td>
<td width="60%">
The machine is a stand-alone system.

</td>
</tr>
</table>

### -field SetupMode

Contains a nonzero value if setup is running.

### -field DomainSid

The security identifier of the primary domain.

### -field DomainName

The name of the primary domain.

### -field DnsDomainName

The Domain Name System (DNS) name of the primary domain.

### -field DomainGuid

The GUID of the primary domain.