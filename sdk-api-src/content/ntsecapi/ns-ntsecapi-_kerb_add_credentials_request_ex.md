---
UID: NS:ntsecapi._KERB_ADD_CREDENTIALS_REQUEST_EX
title: "_KERB_ADD_CREDENTIALS_REQUEST_EX"
author: windows-sdk-content
description: Specifies a message to add, remove, or replace an extra server credential for a logon session, and the service principal names (SPNs) to be associated with that credential.
old-location: security\kerb_add_credentials_request_ex.htm
tech.root: secauthn
ms.assetid: 9e806fce-9b3e-4bc9-bd75-a692f0ca5680
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PKERB_ADD_CREDENTIALS_REQUEST_EX, KERB_ADD_CREDENTIALS_REQUEST_EX, KERB_ADD_CREDENTIALS_REQUEST_EX structure [Security], PKERB_ADD_CREDENTIALS_REQUEST_EX, PKERB_ADD_CREDENTIALS_REQUEST_EX structure pointer [Security], _KERB_ADD_CREDENTIALS_REQUEST_EX, ntsecapi/KERB_ADD_CREDENTIALS_REQUEST_EX, ntsecapi/PKERB_ADD_CREDENTIALS_REQUEST_EX, security.kerb_add_credentials_request_ex"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_ADD_CREDENTIALS_REQUEST_EX
product: Windows
targetos: Windows
req.typenames: KERB_ADD_CREDENTIALS_REQUEST_EX, *PKERB_ADD_CREDENTIALS_REQUEST_EX
req.redist: 
---

# _KERB_ADD_CREDENTIALS_REQUEST_EX structure


## -description


Specifies a  message to add, remove, or replace an extra server credential for a logon session, and 
the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">service principal names</a> (SPNs) to be associated with that 
credential. The <b>SeTcbPrivilege</b> constant is required to alter another logon account's credentials.


## -struct-fields




### -field Credentials

A <a href="https://msdn.microsoft.com/a9a8810b-c9cf-4e19-8a33-7ad0c7ef8694">KERB_ADD_CREDENTIALS_REQUEST</a> structure that specifies the credentials to add, remove, or replace.


### -field PrincipalNameCount

The number of elements in the <b>PrincipalNames</b> array.


### -field PrincipalNames

An array of SPNs to be associated with the user account specified by the <b>Credentials</b> member


## -remarks



Calling the   <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function with this structure affects only the behavior of the <a href="https://msdn.microsoft.com/838eaaa7-6fce-4ed1-bd69-6e76a804c67b">AcceptSecurityContext (Kerberos)</a> function. Using this structure allows multiple physical and virtual servers to share a single identity.




## -see-also




<a href="https://msdn.microsoft.com/a9a8810b-c9cf-4e19-8a33-7ad0c7ef8694">KERB_ADD_CREDENTIALS_REQUEST</a>
 

 

