---
UID: NF:ntsecapi.LsaUnregisterPolicyChangeNotification
title: LsaUnregisterPolicyChangeNotification function (ntsecapi.h)
description: The LsaUnregisterPolicyChangeNotification function disables a previously registered notification event.
helpviewer_keywords: ["LsaUnregisterPolicyChangeNotification","LsaUnregisterPolicyChangeNotification function [Security]","PolicyNotifyAccountDomainInformation","PolicyNotifyAuditEventsInformation","PolicyNotifyDnsDomainInformation","PolicyNotifyDomainEfsInformation","PolicyNotifyDomainKerberosTicketInformation","PolicyNotifyServerRoleInformation","_lsa_lsaunregisterpolicychangenotification","ntsecapi/LsaUnregisterPolicyChangeNotification","security.lsaunregisterpolicychangenotification"]
old-location: security\lsaunregisterpolicychangenotification.htm
tech.root: security
ms.assetid: c1000904-20a6-40db-9b59-2cbb79e00a67
ms.date: 12/05/2018
ms.keywords: LsaUnregisterPolicyChangeNotification, LsaUnregisterPolicyChangeNotification function [Security], PolicyNotifyAccountDomainInformation, PolicyNotifyAuditEventsInformation, PolicyNotifyDnsDomainInformation, PolicyNotifyDomainEfsInformation, PolicyNotifyDomainKerberosTicketInformation, PolicyNotifyServerRoleInformation, _lsa_lsaunregisterpolicychangenotification, ntsecapi/LsaUnregisterPolicyChangeNotification, security.lsaunregisterpolicychangenotification
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaUnregisterPolicyChangeNotification
 - ntsecapi/LsaUnregisterPolicyChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaUnregisterPolicyChangeNotification
---

# LsaUnregisterPolicyChangeNotification function


## -description

The <b>LsaUnregisterPolicyChangeNotification</b> function disables a previously registered notification event.

## -parameters

### -param InformationClass [in]

A 
<a href="/windows/win32/api/ntsecapi/ne-ntsecapi-policy_notification_information_class">POLICY_NOTIFICATION_INFORMATION_CLASS</a> value that specifies the policy changes that your application will stop receiving notifications for. Specify one of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyAuditEventsInformation"></a><a id="policynotifyauditeventsinformation"></a><a id="POLICYNOTIFYAUDITEVENTSINFORMATION"></a><dl>
<dt><b>PolicyNotifyAuditEventsInformation</b></dt>
</dl>
</td>
<td width="60%">
Auditing policy changes.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyAccountDomainInformation"></a><a id="policynotifyaccountdomaininformation"></a><a id="POLICYNOTIFYACCOUNTDOMAININFORMATION"></a><dl>
<dt><b>PolicyNotifyAccountDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Account domain information changes.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyServerRoleInformation"></a><a id="policynotifyserverroleinformation"></a><a id="POLICYNOTIFYSERVERROLEINFORMATION"></a><dl>
<dt><b>PolicyNotifyServerRoleInformation</b></dt>
</dl>
</td>
<td width="60%">
Server role changes.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyDomainEfsInformation"></a><a id="policynotifydomainefsinformation"></a><a id="POLICYNOTIFYDOMAINEFSINFORMATION"></a><dl>
<dt><b>PolicyNotifyDomainEfsInformation</b></dt>
</dl>
</td>
<td width="60%">
EFS policy information changes.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyDomainKerberosTicketInformation"></a><a id="policynotifydomainkerberosticketinformation"></a><a id="POLICYNOTIFYDOMAINKERBEROSTICKETINFORMATION"></a><dl>
<dt><b>PolicyNotifyDomainKerberosTicketInformation</b></dt>
</dl>
</td>
<td width="60%">
Kerberos ticket policy information changes.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyNotifyDnsDomainInformation"></a><a id="policynotifydnsdomaininformation"></a><a id="POLICYNOTIFYDNSDOMAININFORMATION"></a><dl>
<dt><b>PolicyNotifyDnsDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Domain Name System (DNS) information, name, or SID of the system's primary domain changes.

</td>
</tr>
</table>

### -param NotificationEventHandle [in]

A handle to the notification event to unregister.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

For an example that demonstrates calling this function see 
<a href="/windows/desktop/SecMgmt/receiving-policy-change-events">Receiving Policy Change Events</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification">LsaRegisterPolicyChangeNotification</a>