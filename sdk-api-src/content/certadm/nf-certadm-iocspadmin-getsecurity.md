---
UID: NF:certadm.IOCSPAdmin.GetSecurity
title: IOCSPAdmin::GetSecurity (certadm.h)
description: Gets security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.
helpviewer_keywords: ["GetSecurity","GetSecurity method [Security]","GetSecurity method [Security]","IOCSPAdmin interface","IOCSPAdmin interface [Security]","GetSecurity method","IOCSPAdmin.GetSecurity","IOCSPAdmin::GetSecurity","certadm/IOCSPAdmin::GetSecurity","security.iocspadmin_getsecurity"]
old-location: security\iocspadmin_getsecurity.htm
tech.root: security
ms.assetid: 0859ea85-66b2-45af-9559-c81e6a766cfc
ms.date: 12/05/2018
ms.keywords: GetSecurity, GetSecurity method [Security], GetSecurity method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetSecurity method, IOCSPAdmin.GetSecurity, IOCSPAdmin::GetSecurity, certadm/IOCSPAdmin::GetSecurity, security.iocspadmin_getsecurity
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
 - IOCSPAdmin::GetSecurity
 - certadm/IOCSPAdmin::GetSecurity
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
 - IOCSPAdmin.GetSecurity
---

# IOCSPAdmin::GetSecurity


## -description

The <b>GetSecurity</b> method gets security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param pVal [out]

## -returns

<h3>C++</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The security descriptor information.

## -remarks

This method calls the <a href="/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> function to create a string value in <a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>