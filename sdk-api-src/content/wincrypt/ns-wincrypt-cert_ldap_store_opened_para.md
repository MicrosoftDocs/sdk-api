---
UID: NS:wincrypt._CERT_LDAP_STORE_OPENED_PARA
title: CERT_LDAP_STORE_OPENED_PARA
author: windows-sdk-content
description: Used with the CertOpenStore function when the CERT_STORE_PROV_LDAP provider is specified by using the CERT_LDAP_STORE_OPENED_FLAG flag to specify both the existing LDAP session to use to perform the query as well as the LDAP query string.
old-location: security\cert_ldap_store_opened_para.htm
tech.root: seccrypto
ms.assetid: f13b8181-6173-44f8-ab30-4311042cd1b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_LDAP_STORE_OPENED_PARA, CERT_LDAP_STORE_OPENED_PARA, CERT_LDAP_STORE_OPENED_PARA structure [Security], PCERT_LDAP_STORE_OPENED_PARA, PCERT_LDAP_STORE_OPENED_PARA structure pointer [Security], security.cert_ldap_store_opened_para, wincrypt/CERT_LDAP_STORE_OPENED_PARA, wincrypt/PCERT_LDAP_STORE_OPENED_PARA"
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LDAP_STORE_OPENED_PARA
product: Windows
targetos: Windows
req.typenames: CERT_LDAP_STORE_OPENED_PARA, *PCERT_LDAP_STORE_OPENED_PARA
req.redist: 
---

# CERT_LDAP_STORE_OPENED_PARA structure


## -description


The <b>CERT_LDAP_STORE_OPENED_PARA</b> structure is used with the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function when the <b>CERT_STORE_PROV_LDAP</b> provider is specified by using the <b>CERT_LDAP_STORE_OPENED_FLAG</b> flag to specify both the existing LDAP session to use to perform the query as well as the LDAP query string.


## -struct-fields




### -field pvLdapSessionHandle

The handle of the existing LDAP session. This is the handle that is returned by the <a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a> function.


### -field pwszLdapUrl

The address of a null-terminated Unicode string that contains the LDAP query string. For more information about LDAP query strings, see <a href="https://msdn.microsoft.com/29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f">LDAP Dialect</a>.


## -see-also




<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>
 

 

