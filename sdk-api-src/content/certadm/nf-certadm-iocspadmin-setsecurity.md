---
UID: NF:certadm.IOCSPAdmin.SetSecurity
title: IOCSPAdmin::SetSecurity (certadm.h)
description: Updates security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.
helpviewer_keywords: ["IOCSPAdmin interface [Security]","SetSecurity method","IOCSPAdmin.SetSecurity","IOCSPAdmin::SetSecurity","SetSecurity","SetSecurity method [Security]","SetSecurity method [Security]","IOCSPAdmin interface","certadm/IOCSPAdmin::SetSecurity","security.iocspadmin_setsecurity"]
old-location: security\iocspadmin_setsecurity.htm
tech.root: security
ms.assetid: 7ff94496-4347-4c08-8c71-0c53af902d9d
ms.date: 12/05/2018
ms.keywords: IOCSPAdmin interface [Security],SetSecurity method, IOCSPAdmin.SetSecurity, IOCSPAdmin::SetSecurity, SetSecurity, SetSecurity method [Security], SetSecurity method [Security],IOCSPAdmin interface, certadm/IOCSPAdmin::SetSecurity, security.iocspadmin_setsecurity
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::SetSecurity
 - certadm/IOCSPAdmin::SetSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.SetSecurity
---

# IOCSPAdmin::SetSecurity


## -description

The <b>SetSecurity</b> method updates security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param bstrVal [in]

A string that contains the security descriptor information to assign to the responder server.

## -remarks

This method calls the <a href="/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora">ConvertStringSecurityDescriptorToSecurityDescriptor</a> function to create a security descriptor from a string in <a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>