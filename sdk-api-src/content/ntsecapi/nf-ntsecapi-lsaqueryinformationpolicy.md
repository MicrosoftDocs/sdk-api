---
UID: NF:ntsecapi.LsaQueryInformationPolicy
title: LsaQueryInformationPolicy function (ntsecapi.h)
description: Retrieves information about a Policy object.
helpviewer_keywords: ["LsaQueryInformationPolicy","LsaQueryInformationPolicy function [Security]","PolicyAccountDomainInformation","PolicyAuditEventsInformation","PolicyDnsDomainInformation","PolicyLsaServerRoleInformation","PolicyModificationInformation","PolicyPrimaryDomainInformation","_lsa_lsaqueryinformationpolicy","ntsecapi/LsaQueryInformationPolicy","security.lsaqueryinformationpolicy"]
old-location: security\lsaqueryinformationpolicy.htm
tech.root: security
ms.assetid: 2d543500-f639-4ef7-91f4-cdc5060dd567
ms.date: 12/05/2018
ms.keywords: LsaQueryInformationPolicy, LsaQueryInformationPolicy function [Security], PolicyAccountDomainInformation, PolicyAuditEventsInformation, PolicyDnsDomainInformation, PolicyLsaServerRoleInformation, PolicyModificationInformation, PolicyPrimaryDomainInformation, _lsa_lsaqueryinformationpolicy, ntsecapi/LsaQueryInformationPolicy, security.lsaqueryinformationpolicy
req.header: ntsecapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaQueryInformationPolicy
 - ntsecapi/LsaQueryInformationPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsapolicy-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaQueryInformationPolicy
---

# LsaQueryInformationPolicy function


## -description

The <b>LsaQueryInformationPolicy</b> function retrieves information about a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The required access rights for this handle depend on the value of the <i>InformationClass</i> parameter. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param InformationClass [in]

Specifies one of the following values from the 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information to retrieve. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyAuditEventsInformation"></a><a id="policyauditeventsinformation"></a><a id="POLICYAUDITEVENTSINFORMATION"></a><dl>
<dt><b>PolicyAuditEventsInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the system's auditing rules. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_AUDIT_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_events_info">POLICY_AUDIT_EVENTS_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyPrimaryDomainInformation"></a><a id="policyprimarydomaininformation"></a><a id="POLICYPRIMARYDOMAININFORMATION"></a><dl>
<dt><b>PolicyPrimaryDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name and SID of the system's primary domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_LOCAL_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyAccountDomainInformation"></a><a id="policyaccountdomaininformation"></a><a id="POLICYACCOUNTDOMAININFORMATION"></a><dl>
<dt><b>PolicyAccountDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name and SID of the system's account domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_LOCAL_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_account_domain_info">POLICY_ACCOUNT_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyLsaServerRoleInformation"></a><a id="policylsaserverroleinformation"></a><a id="POLICYLSASERVERROLEINFORMATION"></a><dl>
<dt><b>PolicyLsaServerRoleInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the role of an LSA server. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_LOCAL_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyModificationInformation"></a><a id="policymodificationinformation"></a><a id="POLICYMODIFICATIONINFORMATION"></a><dl>
<dt><b>PolicyModificationInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves information about the creation time and last modification of the LSA database. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_LOCAL_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_modification_info">POLICY_MODIFICATION_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyDnsDomainInformation"></a><a id="policydnsdomaininformation"></a><a id="POLICYDNSDOMAININFORMATION"></a><dl>
<dt><b>PolicyDnsDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the Domain Name System (DNS) information about the primary domain associated with the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_VIEW_LOCAL_INFORMATION access right. The <i>Buffer</i> parameter receives a pointer to a 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a> structure.

</td>
</tr>
</table>

### -param Buffer [out]

Pointer to a variable that receives a pointer to a structure containing the requested information. The type of structure depends on the value of the <i>InformationClass</i> parameter. 




When you no longer need the information, pass the returned pointer to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.

## -returns

If the <b>LsaQueryInformationPolicy</b> function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

For an example that demonstrates calling this function see 
<a href="/windows/desktop/SecMgmt/managing-policy-information">Managing Policy Information</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_account_domain_info">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_events_info">POLICY_AUDIT_EVENTS_INFO</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-policy_dns_domain_info">POLICY_DNS_DOMAIN_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_lsa_server_role_info">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_modification_info">POLICY_MODIFICATION_INFO</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_primary_domain_info">POLICY_PRIMARY_DOMAIN_INFO</a>