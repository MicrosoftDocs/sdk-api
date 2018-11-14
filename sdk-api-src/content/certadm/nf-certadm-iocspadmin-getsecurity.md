---
UID: NF:certadm.IOCSPAdmin.GetSecurity
title: IOCSPAdmin::GetSecurity
author: windows-sdk-content
description: Gets security descriptor information for an Online Certificate Status Protocol (OCSP) responder server.
old-location: security\iocspadmin_getsecurity.htm
tech.root: seccrypto
ms.assetid: 0859ea85-66b2-45af-9559-c81e6a766cfc
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetSecurity, GetSecurity method [Security], GetSecurity method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetSecurity method, IOCSPAdmin.GetSecurity, IOCSPAdmin::GetSecurity, certadm/IOCSPAdmin::GetSecurity, security.iocspadmin_getsecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certadm.h
: 
- IOCSPAdmin.GetSecurity
: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The security descriptor information.



## -remarks



This method calls the <a href="https://msdn.microsoft.com/36140833-8e30-4c32-a88a-c10751b6c223">ConvertSecurityDescriptorToStringSecurityDescriptor</a> function to create a string value in <a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a>
 

 

