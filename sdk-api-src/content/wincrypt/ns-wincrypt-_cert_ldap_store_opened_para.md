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

# _CERT_LDAP_STORE_OPENED_PARA structure


## -description


The <b>CERT_LDAP_STORE_OPENED_PARA</b> structure is used with the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function when the <b>CERT_STORE_PROV_LDAP</b> provider is specified by using the <b>CERT_LDAP_STORE_OPENED_FLAG</b> flag to specify both the existing LDAP session to use to perform the query as well as the LDAP query string.


## -struct-fields




### -field pvLdapSessionHandle

The handle of the existing LDAP session. This is the handle that is returned by the <a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a> function.


### -field pwszLdapUrl

The address of a null-terminated Unicode string that contains the LDAP query string. For more information about LDAP query strings, see <a href="https://msdn.microsoft.com/29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f">LDAP Dialect</a>.


## -see-also




<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>
 

 

