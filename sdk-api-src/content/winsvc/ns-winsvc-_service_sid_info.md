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

# _SERVICE_SID_INFO structure


## -description


Represents a service security identifier (SID).


## -struct-fields




### -field dwServiceSidType

The service SID type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_SID_TYPE_NONE"></a><a id="service_sid_type_none"></a><dl>
<dt><b>SERVICE_SID_TYPE_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Use this type to reduce application compatibility issues.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_SID_TYPE_RESTRICTED"></a><a id="service_sid_type_restricted"></a><dl>
<dt><b>SERVICE_SID_TYPE_RESTRICTED</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
This type includes SERVICE_SID_TYPE_UNRESTRICTED. The service SID is also added to the restricted SID list of the process token. Three additional SIDs are also added to the restricted SID list: 

<ul>
<li>World SID S-1-1-0</li>
<li>Service logon SID</li>
<li>Write-restricted SID S-1-5-33</li>
</ul>
One ACE that allows GENERIC_ALL access for the service logon SID is also added to the service process token object.

If there are multiple services hosted in the same process and one service has SERVICE_SID_TYPE_RESTRICTED, all services must have SERVICE_SID_TYPE_RESTRICTED.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_SID_TYPE_UNRESTRICTED"></a><a id="service_sid_type_unrestricted"></a><dl>
<dt><b>SERVICE_SID_TYPE_UNRESTRICTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
When the service process is created, the service SID is added to the service process token with the following attributes: SE_GROUP_ENABLED_BY_DEFAULT | SE_GROUP_OWNER.

</td>
</tr>
</table>
 


## -remarks



The change takes effect the next time the system is started.

The SCM adds the specified service SIDs to the process token, plus the following additional SIDs.

<table>
<tr>
<th>SID</th>
<th>Attributes</th>
</tr>
<tr>
<td>Logon SID</td>
<td>SE_GROUP_ENABLED | SE_GROUP_ENABLED_BY_DEFAULT | SE_GROUP_LOGON_ID | SE_GROUP_MANDATORY</td>
</tr>
<tr>
<td>Local SID</td>
<td>SE_GROUP_MANDATORY | SE_GROUP_ENABLED | SE_GROUP_ENABLED_BY_DEFAULT</td>
</tr>
</table>
 

This enables developers to control access to the objects a service uses, instead of relying on the use of the LocalSystem account to obtain access.

Use the <a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a> and <a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a> functions to convert between a service name and a service SID. The account name is of the following form:

NT SERVICE\<i>SvcName</i>

Note that NT SERVICE is the domain name.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 

