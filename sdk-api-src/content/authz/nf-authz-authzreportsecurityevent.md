---
UID: NF:authz.AuthzReportSecurityEvent
title: AuthzReportSecurityEvent function (authz.h)
description: Generates a security audit for a registered security event source.
helpviewer_keywords: ["APF_AuditFailure","APF_AuditSuccess","AuthzReportSecurityEvent","AuthzReportSecurityEvent function [Security]","authz/AuthzReportSecurityEvent","security.authzreportsecurityevent"]
old-location: security\authzreportsecurityevent.htm
tech.root: security
ms.assetid: 95d561ef-3233-433a-a1e7-b914df1dd211
ms.date: 12/05/2018
ms.keywords: APF_AuditFailure, APF_AuditSuccess, AuthzReportSecurityEvent, AuthzReportSecurityEvent function [Security], authz/AuthzReportSecurityEvent, security.authzreportsecurityevent
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - AuthzReportSecurityEvent
 - authz/AuthzReportSecurityEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzReportSecurityEvent
---

# AuthzReportSecurityEvent function


## -description

The <b>AuthzReportSecurityEvent</b> function generates a security audit for a registered security event source.

Auditing for the  object access event category must be enabled for the <b>AuthzReportSecurityEvent</b> function to generate a security audit. The available audit types are defined in the <a href="/windows/desktop/api/adtgen/ne-adtgen-audit_param_type">AUDIT_PARAM_TYPE</a> enumeration.

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

A pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that will be listed as the source of the audit in the event log.

### -param dwCount [in]

The number of AuditParamFlag  type/value pairs that appear in the variable arguments section that follows this parameter.

### -param ...

A list of AuditParamFlag type/value pairs that provide additional information about the event.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzregistersecurityeventsource">AuthzRegisterSecurityEventSource</a>



<a href="/windows/desktop/api/authz/nf-authz-authzreportsecurityeventfromparams">AuthzReportSecurityEventFromParams</a>

