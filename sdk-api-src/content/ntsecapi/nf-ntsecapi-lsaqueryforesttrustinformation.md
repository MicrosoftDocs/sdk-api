---
UID: NF:ntsecapi.LsaQueryForestTrustInformation
title: LsaQueryForestTrustInformation function (ntsecapi.h)
description: Retrieves forest trust information for the specified Local Security Authority�TrustedDomain object.
helpviewer_keywords: ["LsaQueryForestTrustInformation","LsaQueryForestTrustInformation function [Security]","ntsecapi/LsaQueryForestTrustInformation","security.lsaqueryforesttrustinformation"]
old-location: security\lsaqueryforesttrustinformation.htm
tech.root: security
ms.assetid: 38857f1f-e2c7-4ce5-a928-335bc3bd2176
ms.date: 12/05/2018
ms.keywords: LsaQueryForestTrustInformation, LsaQueryForestTrustInformation function [Security], ntsecapi/LsaQueryForestTrustInformation, security.lsaqueryforesttrustinformation
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
 - LsaQueryForestTrustInformation
 - ntsecapi/LsaQueryForestTrustInformation
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
 - LsaQueryForestTrustInformation
---

# LsaQueryForestTrustInformation function


## -description

The <b>LsaQueryForestTrustInformation</b> function retrieves forest trust information
    for the specified <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object for the system.

### -param TrustedDomainName [in]

Pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object for which to retrieve forest trust information.

### -param ForestTrustInfo [out]

Pointer to an <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_information">LSA_FOREST_TRUST_INFORMATION</a> structure that returns the forest trust information for the <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object specified by the <i>TrustedDomainName</i> parameter.

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
<dt><b>STATUS_INVALID_DOMAIN_ROLE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The operation is legal only on the primary
                                    domain controller.

</td>
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
<dt><b>STATUS_NO_SUCH_DOMAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The specified <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The specified <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object does not contain forest trust information.

</td>
</tr>
</table>

## -remarks

Access to this function is protected by a securable object.