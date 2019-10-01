---
UID: NF:certadm.IOCSPAdmin.GetSecurity
title: IOCSPAdmin::GetSecurity (certadm.h)
author: windows-sdk-content
description: Gets security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.
old-location: security\iocspadmin_getsecurity.htm
tech.root: SecCrypto
ms.assetid: 0859ea85-66b2-45af-9559-c81e6a766cfc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSecurity, GetSecurity method [Security], GetSecurity method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetSecurity method, IOCSPAdmin.GetSecurity, IOCSPAdmin::GetSecurity, certadm/IOCSPAdmin::GetSecurity, security.iocspadmin_getsecurity
ms.topic: method
f1_keywords: 
 - "certadm/IOCSPAdmin.GetSecurity"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.GetSecurity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The security descriptor information.



## -remarks



This method calls the <a href="https://docs.microsoft.com/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora">ConvertSecurityDescriptorToStringSecurityDescriptor</a> function to create a string value in <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>
 

 

