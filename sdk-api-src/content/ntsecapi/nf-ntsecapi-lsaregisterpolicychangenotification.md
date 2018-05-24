---
UID: NF:ntsecapi.LsaRegisterPolicyChangeNotification
title: LsaRegisterPolicyChangeNotification function
author: windows-driver-content
description: The LsaRegisterPolicyChangeNotification function registers an event handle with the local security authority (LSA). This event handle is signaled whenever the indicated LSA policy is modified.
old-location: security\lsaregisterpolicychangenotification.htm
old-project: SecMgmt
ms.assetid: 0c713d2b-e13a-44e0-8b48-68b233d1c562
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: LsaRegisterPolicyChangeNotification, LsaRegisterPolicyChangeNotification function [Security], PolicyNotifyAccountDomainInformation, PolicyNotifyAuditEventsInformation, PolicyNotifyDnsDomainInformation, PolicyNotifyDomainEfsInformation, PolicyNotifyDomainKerberosTicketInformation, PolicyNotifyServerRoleInformation, _lsa_lsaregisterpolicychangenotification, ntsecapi/LsaRegisterPolicyChangeNotification, security.lsaregisterpolicychangenotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Secur32.dll
api_name:
-	LsaRegisterPolicyChangeNotification
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LsaRegisterPolicyChangeNotification function


## -description


The <b>LsaRegisterPolicyChangeNotification</b> function registers an event handle with the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">local security authority</a> (LSA). This event handle is signaled whenever the indicated LSA policy is modified.


## -parameters




### -param InformationClass [in]

A 
<a href="https://msdn.microsoft.com/cf8eea7a-d3b0-4c3a-b05b-3027024ab025">POLICY_NOTIFICATION_INFORMATION_CLASS</a> value that specifies the type of policy changes about which your application will be notified. Specify one of the following values. 




					

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
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. The event can be either named or unnamed.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



When you have finished using a notification event that has been registered by the <b>LsaRegisterPolicyChangeNotification</b> function, unregister it by calling the <a href="https://msdn.microsoft.com/c1000904-20a6-40db-9b59-2cbb79e00a67">LsaUnregisterPolicyChangeNotification</a> function.

For an example that demonstrates calling this function, see 
<a href="https://msdn.microsoft.com/29c693f5-db2b-4fda-847c-4e5220eadfd3">Receiving Policy Change Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1000904-20a6-40db-9b59-2cbb79e00a67">LsaUnregisterPolicyChangeNotification</a>
 

 

