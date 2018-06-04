---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# LsaUnregisterPolicyChangeNotification function


## -description


The <b>LsaUnregisterPolicyChangeNotification</b> function disables a previously registered notification event.


## -parameters




### -param InformationClass [in]

A 
<a href="https://msdn.microsoft.com/cf8eea7a-d3b0-4c3a-b05b-3027024ab025">POLICY_NOTIFICATION_INFORMATION_CLASS</a> value that specifies the policy changes that your application will stop receiving notifications for. Specify one of the following values. 





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
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



For an example that demonstrates calling this function see 
<a href="https://msdn.microsoft.com/29c693f5-db2b-4fda-847c-4e5220eadfd3">Receiving Policy Change Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/0c713d2b-e13a-44e0-8b48-68b233d1c562">LsaRegisterPolicyChangeNotification</a>
 

 

