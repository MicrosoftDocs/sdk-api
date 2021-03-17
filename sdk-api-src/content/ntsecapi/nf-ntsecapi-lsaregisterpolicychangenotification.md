---
UID: NF:ntsecapi.LsaRegisterPolicyChangeNotification
title: LsaRegisterPolicyChangeNotification function (ntsecapi.h)
description: The LsaRegisterPolicyChangeNotification function registers an event handle with the local security authority (LSA). This event handle is signaled whenever the indicated LSA policy is modified.
helpviewer_keywords: ["LsaRegisterPolicyChangeNotification","LsaRegisterPolicyChangeNotification function [Security]","PolicyNotifyAccountDomainInformation","PolicyNotifyAuditEventsInformation","PolicyNotifyDnsDomainInformation","PolicyNotifyDomainEfsInformation","PolicyNotifyDomainKerberosTicketInformation","PolicyNotifyServerRoleInformation","_lsa_lsaregisterpolicychangenotification","ntsecapi/LsaRegisterPolicyChangeNotification","security.lsaregisterpolicychangenotification"]
old-location: security\lsaregisterpolicychangenotification.htm
tech.root: security
ms.assetid: 0c713d2b-e13a-44e0-8b48-68b233d1c562
ms.date: 12/05/2018
ms.keywords: LsaRegisterPolicyChangeNotification, LsaRegisterPolicyChangeNotification function [Security], PolicyNotifyAccountDomainInformation, PolicyNotifyAuditEventsInformation, PolicyNotifyDnsDomainInformation, PolicyNotifyDomainEfsInformation, PolicyNotifyDomainKerberosTicketInformation, PolicyNotifyServerRoleInformation, _lsa_lsaregisterpolicychangenotification, ntsecapi/LsaRegisterPolicyChangeNotification, security.lsaregisterpolicychangenotification
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
 - LsaRegisterPolicyChangeNotification
 - ntsecapi/LsaRegisterPolicyChangeNotification
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
 - LsaRegisterPolicyChangeNotification
---

# LsaRegisterPolicyChangeNotification function


## -description

The <b>LsaRegisterPolicyChangeNotification</b> function registers an event handle with the <a href="/windows/desktop/SecGloss/l-gly">local security authority</a> (LSA). This event handle is signaled whenever the indicated LSA policy is modified.

## -parameters

### -param InformationClass [in]

A 
<a href="/windows/win32/api/ntsecapi/ne-ntsecapi-policy_notification_information_class">POLICY_NOTIFICATION_INFORMATION_CLASS</a> value that specifies the type of policy changes about which your application will be notified. Specify one of the following values. 




					

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

A handle to an event obtained by calling the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function. The event can be either named or unnamed.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -remarks

When you have finished using a notification event that has been registered by the <b>LsaRegisterPolicyChangeNotification</b> function, unregister it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification">LsaUnregisterPolicyChangeNotification</a> function.

For an example that demonstrates calling this function, see 
<a href="/windows/desktop/SecMgmt/receiving-policy-change-events">Receiving Policy Change Events</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification">LsaUnregisterPolicyChangeNotification</a>