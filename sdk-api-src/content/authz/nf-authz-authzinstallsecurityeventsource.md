---
UID: NF:authz.AuthzInstallSecurityEventSource
title: AuthzInstallSecurityEventSource function (authz.h)
description: Installs the specified source as a security event source.
helpviewer_keywords: ["AuthzInstallSecurityEventSource","AuthzInstallSecurityEventSource function [Security]","authz/AuthzInstallSecurityEventSource","security.authzinstallsecurityeventsource"]
old-location: security\authzinstallsecurityeventsource.htm
tech.root: security
ms.assetid: 77cb5c6c-1634-4449-8d05-ce6357ad4e4b
ms.date: 12/05/2018
ms.keywords: AuthzInstallSecurityEventSource, AuthzInstallSecurityEventSource function [Security], authz/AuthzInstallSecurityEventSource, security.authzinstallsecurityeventsource
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
 - AuthzInstallSecurityEventSource
 - authz/AuthzInstallSecurityEventSource
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
 - AuthzInstallSecurityEventSource
---

# AuthzInstallSecurityEventSource function


## -description

The <b>AuthzInstallSecurityEventSource</b> function installs  the specified source as a security event source.

## -parameters

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.

### -param pRegistration [in]

A pointer to an <a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure that contains information about the security event source to be added.

The members of the <a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure are used as follows to install the security event source in the security log key:

<ul>
<li>The <b>szEventSourceName</b> member is added as a registry key under <pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SYSTEM</b>
      <b>CurrentControlSet</b>
         <b>Services</b>
            <b>EventLog</b>
               <b>Security</b></pre>
</li>
<li>The <b>szEventMessageFile</b> member is added as the data in a REG_SZ value named <b>EventMessageFile</b> under the event source key.</li>
<li>The <b>szEventAccessStringsFile</b> member is added as the data in a REG_SZ value named <b>ParameterMessageFile</b> under the event source key.</li>
<li>If the registry path does not exist, it is created.</li>
</ul>
<ul>
<li>If the <b>szEventSourceXmlSchemaFile</b> member is not <b>NULL</b>, it is added as the data in a REG_SZ value named <b>XmlSchemaFile</b> under the event source key. This value is not used.</li>
<li>The <b>szExecutableImagePath</b> member may be set to <b>NULL</b>.</li>
</ul>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>



<a href="/windows/desktop/api/authz/nf-authz-authzuninstallsecurityeventsource">AuthzUninstallSecurityEventSource</a>
