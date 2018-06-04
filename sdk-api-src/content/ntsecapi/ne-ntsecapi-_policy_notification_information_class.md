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

# _POLICY_NOTIFICATION_INFORMATION_CLASS enumeration


## -description


The <b>POLICY_NOTIFICATION_INFORMATION_CLASS</b> enumeration defines the types of policy information and policy domain information for which your application can request notification of changes.


## -enum-fields




### -field PolicyNotifyAuditEventsInformation

Notify when any of the audited categories are changed.


### -field PolicyNotifyAccountDomainInformation

Notify when the account domain information changes.


### -field PolicyNotifyServerRoleInformation

Notify when the LSA server changes its role from primary to backup, or vice versa.


### -field PolicyNotifyDnsDomainInformation

Notify when the DNS domain information changes or if the primary domain information changes.


### -field PolicyNotifyDomainEfsInformation

Notify when the Encrypting File System (EFS) domain information changes.


### -field PolicyNotifyDomainKerberosTicketInformation

Notify when the Kerberos ticket for the domain changes.


### -field PolicyNotifyMachineAccountPasswordInformation

Notify when the machine account password changes.


### -field PolicyNotifyGlobalSaclInformation


### -field PolicyNotifyMax




## -see-also




<a href="https://msdn.microsoft.com/0c713d2b-e13a-44e0-8b48-68b233d1c562">LsaRegisterPolicyChangeNotification</a>



<a href="https://msdn.microsoft.com/c1000904-20a6-40db-9b59-2cbb79e00a67">LsaUnregisterPolicyChangeNotification</a>
 

 

