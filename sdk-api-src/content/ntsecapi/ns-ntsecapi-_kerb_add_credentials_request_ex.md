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
 

 

