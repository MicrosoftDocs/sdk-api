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

# tag_WBEM_SECURITY_FLAGS enumeration


## -description


Contains flags used for setting security access levels.


## -enum-fields




### -field WBEM_ENABLE

Enables the account and grants the user read permissions. This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the <a href="gloss_w.htm">WMI Control</a>. For more information, see <a href="https://msdn.microsoft.com/87c23919-c482-4278-b005-894a8ac21da4">Setting Namespace Security with the WMI Control</a>.


### -field WBEM_METHOD_EXECUTE

Allows the execution of methods. 


 Providers can perform additional access checks. This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.


### -field WBEM_FULL_WRITE_REP

Allows a user account to write to classes in the WMI repository as well as instances. A user cannot write to system classes. Only members of the Administrators group have this permission. <b>WBEM_FULL_WRITE_REP</b> corresponds to the Full Write permission on the Security tab of the WMI Control.


### -field WBEM_PARTIAL_WRITE_REP

Allows you to write data to instances only, not classes. A user cannot write classes to the <a href="gloss_w.htm">WMI repository</a>. Only members of the Administrators group have this right. <b>WBEM_PARTIAL_WRITE_REP</b> corresponds to the Partial Write permission on the Security tab of the WMI Control.


### -field WBEM_WRITE_PROVIDER

Allows writing classes and instances to providers. Note that providers can do additional access checks when impersonating a user. This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.


### -field WBEM_REMOTE_ACCESS

Allows a user account to remotely perform any operations allowed by the permissions described above. Only members of the Administrators group have this right. <b>WBEM_REMOTE_ACCESS</b> corresponds to the Remote Enable permission on the Security tab of the WMI Control.


### -field WBEM_RIGHT_SUBSCRIBE

Specifies that a consumer can subscribe to the events delivered to a sink. Used in <a href="https://msdn.microsoft.com/887b3c21-2ff6-4ae9-80bf-19f601da5e8b">IWbemEventSink::SetSinkSecurity</a>.


### -field WBEM_RIGHT_PUBLISH

Specifies that the account can  publish events to the instance of <a href="https://msdn.microsoft.com/369d3c28-2b69-456f-9144-d7c73e3123bc">__EventFilter</a> that defines the event filter for a permanent consumer. Available in wbemcli.h.


## -see-also




<a href="https://msdn.microsoft.com/18318262-d948-4329-8d48-23664798fc58">Event Security Constants</a>



<a href="https://msdn.microsoft.com/2e905078-d510-4417-8acb-a6ff535d9d0b">Namespace Access Rights Constants</a>
 

 

