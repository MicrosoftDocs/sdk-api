---
UID: NS:wincrypt._CTL_INFO
title: CTL_INFO (wincrypt.h)
description: Contains the information stored in a Certificate Trust List (CTL).
helpviewer_keywords: ["*PCTL_INFO","CTL_INFO","CTL_INFO structure [Security]","CTL_V1","PCTL_INFO","PCTL_INFO structure pointer [Security]","_crypto2_ctl_info","security.ctl_info","wincrypt/CTL_INFO","wincrypt/PCTL_INFO"]
old-location: security\ctl_info.htm
tech.root: security
ms.assetid: 83b015b5-a650-4a81-a9f0-c3e8a9805c81
ms.date: 12/05/2018
ms.keywords: '*PCTL_INFO, CTL_INFO, CTL_INFO structure [Security], CTL_V1, PCTL_INFO, PCTL_INFO structure pointer [Security], _crypto2_ctl_info, security.ctl_info, wincrypt/CTL_INFO, wincrypt/PCTL_INFO'
req.header: wincrypt.h
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
req.typenames: CTL_INFO, *PCTL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_INFO
 - wincrypt/_CTL_INFO
 - PCTL_INFO
 - wincrypt/PCTL_INFO
 - CTL_INFO
 - wincrypt/CTL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_INFO
---

# CTL_INFO structure


## -description

The <b>CTL_INFO</b> structure contains the information stored in a <a href="/windows/desktop/SecGloss/c-gly">Certificate Trust List</a> (CTL).

## -struct-fields

### -field dwVersion

The CTL's version number. Currently defined version numbers are shown in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTL_V1"></a><a id="ctl_v1"></a><dl>
<dt><b>CTL_V1</b></dt>
</dl>
</td>
<td width="60%">
Version 1

</td>
</tr>
</table>

### -field SubjectUsage

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure identifying the intended usage of the list as a sequence of object identifiers. This is the same as in the <a href="/windows/desktop/SecGloss/e-gly">Enhanced Key Usage</a> extension.

### -field ListIdentifier

A
						<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that includes a byte string that uniquely identifies the list. This member is used to augment the <b>SubjectUsage</b> and further specifies the list when desired.

### -field SequenceNumber

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains a monotonically increasing number for each update of the CTL.

### -field ThisUpdate

Indication of the date and time of the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) published. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte year precise to milliseconds with a 4-byte year.

### -field NextUpdate

Indication of the date and time for the CRL's next available scheduled update. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte date time precise to milliseconds with a 4-byte year.

### -field SubjectAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the algorithm type of the <b>SubjectIdentifier</b> in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a> members of the <b>rgCTLEntry</b> member array. The structure also includes additional parameters used by the algorithm.

### -field cCTLEntry

Number of elements in the <b>rgCTLEntry</b> member array.

### -field rgCTLEntry

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a> structures.

### -field cExtension

Number of elements in the <b>rgExtension</b> array.

### -field rgExtension

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a>