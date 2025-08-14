---
UID: NF:ntsecapi.LsaSetForestTrustInformation
title: LsaSetForestTrustInformation function (ntsecapi.h)
description: Sets the forest trust information for a specified Local Security Authority�TrustedDomain object.
helpviewer_keywords: ["LsaSetForestTrustInformation","LsaSetForestTrustInformation function [Security]","ntsecapi/LsaSetForestTrustInformation","security.lsasetforesttrustinformation"]
old-location: security\lsasetforesttrustinformation.htm
tech.root: security
ms.assetid: 8b0f90ed-7dd4-4803-97c6-31d191b6d2b3
ms.date: 12/05/2018
ms.keywords: LsaSetForestTrustInformation, LsaSetForestTrustInformation function [Security], ntsecapi/LsaSetForestTrustInformation, security.lsasetforesttrustinformation
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaSetForestTrustInformation
 - ntsecapi/LsaSetForestTrustInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-lsa-l1-1-4.dll
 - ext-ms-win-advapi32-lsa-l1-1-3.dll
 - ext-ms-win-advapi32-lsa-l1-1-2.dll
 - Advapi32.dll
api_name:
 - LsaSetForestTrustInformation
---

# LsaSetForestTrustInformation function


## -description

The <b>LsaSetForestTrustInformation</b> function sets the forest trust information for a specified <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object for the system.

### -param TrustedDomainName [in]

Pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object to which to set the forest trust information specified by the <i>ForestTrustInfo</i> parameter.

### -param ForestTrustInfo [in]

Pointer to an <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_information">LSA_FOREST_TRUST_INFORMATION</a> structure that contains the forest trust information to set to the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object specified by the <i>TrustedDomainName</i> parameter.

### -param CheckOnly [in]

Boolean value that specifies whether changes to the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object are persisted. If this value is <b>TRUE</b>, this function will check for collisions with the specified parameters but will not set the  forest trust information specified by the <i>ForestTrustInfo</i> parameter to the <b>TrustedDomain</b> object specified by the <i>TrustedDomainName</i> parameter. If this value is <b>FALSE</b>, the forest trust information will be set to the  <b>TrustedDomain</b> object.

### -param CollisionInfo [out]

Pointer to a pointer to an <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_collision_information">LSA_FOREST_TRUST_COLLISION_INFORMATION</a> structure that returns information about any collisions that occurred.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the <a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_STATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The operation is legal only on domain
                                    controllers in the root domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_ROLE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The operation is legal only on the primary
                                    domain controller.

</td>
</tr>
</table>