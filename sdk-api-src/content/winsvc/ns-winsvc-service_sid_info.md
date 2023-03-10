---
UID: NS:winsvc._SERVICE_SID_INFO
title: SERVICE_SID_INFO (winsvc.h)
description: Represents a service security identifier (SID).
helpviewer_keywords: ["*LPSERVICE_SID_INFO","LPSERVICE_SID_INFO","LPSERVICE_SID_INFO structure pointer","SERVICE_SID_INFO","SERVICE_SID_INFO structure","SERVICE_SID_TYPE_NONE","SERVICE_SID_TYPE_RESTRICTED","SERVICE_SID_TYPE_UNRESTRICTED","base.service_sid_info","winsvc/LPSERVICE_SID_INFO","winsvc/SERVICE_SID_INFO"]
old-location: base\service_sid_info.htm
tech.root: security
ms.assetid: cb1a32bd-aafb-4e41-8d6f-673c3d747f14
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_SID_INFO, LPSERVICE_SID_INFO, LPSERVICE_SID_INFO structure pointer, SERVICE_SID_INFO, SERVICE_SID_INFO structure, SERVICE_SID_TYPE_NONE, SERVICE_SID_TYPE_RESTRICTED, SERVICE_SID_TYPE_UNRESTRICTED, base.service_sid_info, winsvc/LPSERVICE_SID_INFO, winsvc/SERVICE_SID_INFO'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_SID_INFO, *LPSERVICE_SID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_SID_INFO
 - winsvc/_SERVICE_SID_INFO
 - LPSERVICE_SID_INFO
 - winsvc/LPSERVICE_SID_INFO
 - SERVICE_SID_INFO
 - winsvc/SERVICE_SID_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_SID_INFO
---

# SERVICE_SID_INFO structure


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

Use the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> and <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a> functions to convert between a service name and a service SID. The account name is of the following form:

NT SERVICE&#92;<i>SvcName</i>

Note that NT SERVICE is the domain name.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>