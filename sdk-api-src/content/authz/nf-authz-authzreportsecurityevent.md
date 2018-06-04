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

# AuthzReportSecurityEvent function


## -description


The <b>AuthzReportSecurityEvent</b> function generates a security audit for a registered security event source.

Auditing for the  object access event category must be enabled for the <b>AuthzReportSecurityEvent</b> function to generate a security audit. The available audit types are defined in the <a href="https://msdn.microsoft.com/1ECC866A-2DD3-4EE4-B2CC-7F5ADF7FFC99">AUDIT_PARAM_TYPE</a> enumeration.


## -parameters




### -param dwFlags [in]

Flags that specify the type of audit generated. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="APF_AuditFailure"></a><a id="apf_auditfailure"></a><a id="APF_AUDITFAILURE"></a><dl>
<dt><b>APF_AuditFailure</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Failure audits are generated.

</td>
</tr>
<tr>
<td width="40%"><a id="APF_AuditSuccess"></a><a id="apf_auditsuccess"></a><a id="APF_AUDITSUCCESS"></a><dl>
<dt><b>APF_AuditSuccess</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Success audits are generated.

</td>
</tr>
</table>
 


### -param hEventProvider [in, out]

A handle to the registered security event source to use for the audit.


### -param dwAuditId [in]

The identifier of the audit.


### -param pUserSid [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that will be listed as the source of the audit in the event log.


### -param dwCount [in]

The number of AuditParamFlag  type/value pairs that appear in the variable arguments section that follows this parameter.


### -param param

TBD




####### - ... [in]

A list of AuditParamFlag type/value pairs that provide additional information about the event.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/726e480d-1a34-4fd6-ac2d-876fa08f4eae">AuthzRegisterSecurityEventSource</a>



<a href="https://msdn.microsoft.com/ee5b598a-0a89-4b32-a9bc-e9c811573b08">AuthzReportSecurityEventFromParams</a>
 

 

