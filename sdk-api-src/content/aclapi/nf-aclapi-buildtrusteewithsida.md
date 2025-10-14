---
UID: NF:aclapi.BuildTrusteeWithSidA
title: BuildTrusteeWithSidA function (aclapi.h)
description: Initializes a TRUSTEE structure. The caller specifies the security identifier (SID) of the trustee. The function sets other members of the structure to default values and does not look up the name associated with the SID. (ANSI)
helpviewer_keywords: ["BuildTrusteeWithSidA", "MultipleTrusteeOperation", "TrusteeForm", "TrusteeType", "aclapi/BuildTrusteeWithSidA", "pMultipleTrustee"]
old-location: security\buildtrusteewithsid.htm
tech.root: security
ms.assetid: 3745fbf2-911a-4cb6-81a8-6256c742c700
ms.date: 12/05/2018
ms.keywords: BuildTrusteeWithSid, BuildTrusteeWithSid function [Security], BuildTrusteeWithSidA, BuildTrusteeWithSidW, MultipleTrusteeOperation, TrusteeForm, TrusteeType, _win32_buildtrusteewithsid, aclapi/BuildTrusteeWithSid, aclapi/BuildTrusteeWithSidA, aclapi/BuildTrusteeWithSidW, pMultipleTrustee, security.buildtrusteewithsid
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildTrusteeWithSidW (Unicode) and BuildTrusteeWithSidA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BuildTrusteeWithSidA
 - aclapi/BuildTrusteeWithSidA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-trustee-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-security-trustee-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
api_name:
 - BuildTrusteeWithSid
 - BuildTrusteeWithSidA
 - BuildTrusteeWithSidW
---

# BuildTrusteeWithSidA function


## -description

The <b>BuildTrusteeWithSid</b> function initializes a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. The caller specifies the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the trustee. The function sets other members of the structure to default values and does not look up the name associated with the SID.

## -parameters

### -param pTrustee [in, out]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure to initialize. The <b>BuildTrusteeWithSid</b> function does not allocate any memory. If this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.

### -param pSid [in, optional]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that identifies the trustee. The <b>BuildTrusteeWithSid</b> function assigns this pointer to the <b>ptstrName</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. The function sets the other members of the <b>TRUSTEE</b> structure as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="pMultipleTrustee"></a><a id="pmultipletrustee"></a><a id="PMULTIPLETRUSTEE"></a><dl>
<dt><b>pMultipleTrustee</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
<tr>
<td width="40%"><a id="MultipleTrusteeOperation"></a><a id="multipletrusteeoperation"></a><a id="MULTIPLETRUSTEEOPERATION"></a><dl>
<dt><b>MultipleTrusteeOperation</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
NO_MULTIPLE_TRUSTEE

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeForm"></a><a id="trusteeform"></a><a id="TRUSTEEFORM"></a><dl>
<dt><b>TrusteeForm</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_SID

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeType"></a><a id="trusteetype"></a><a id="TRUSTEETYPE"></a><dl>
<dt><b>TrusteeType</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_UNKNOWN

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithnamea">BuildTrusteeWithName</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithobjectsandnamea">BuildTrusteeWithObjectsAndName</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithobjectsandsida">BuildTrusteeWithObjectsAndSid</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>

## -remarks

> [!NOTE]
> The aclapi.h header defines BuildTrusteeWithSid as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
