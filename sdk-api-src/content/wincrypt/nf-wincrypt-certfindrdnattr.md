---
UID: NF:wincrypt.CertFindRDNAttr
title: CertFindRDNAttr function (wincrypt.h)
author: windows-sdk-content
description: The CertFindRDNAttr function finds the first RDN attribute identified by its object identifier (OID) in a list of the Relative Distinguished Names (RDN).
old-location: security\certfindrdnattr.htm
tech.root: SecCrypto
ms.assetid: 31f82a02-e90a-48de-857a-9fbb03048b5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertFindRDNAttr, CertFindRDNAttr function [Security], _crypto2_certfindrdnattr, security.certfindrdnattr, wincrypt/CertFindRDNAttr
ms.topic: function
f1_keywords:
- wincrypt/CertFindRDNAttr
dev_langs:
 - c++
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CertFindRDNAttr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertFindRDNAttr function


## -description


The <b>CertFindRDNAttr</b> function finds the first <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">RDN</a> attribute identified by its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) in a list of the <i>Relative Distinguished Names</i> (RDN).


## -parameters




### -param pszObjId [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) to use In the search.


### -param pName [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_name_info">CERT_NAME_INFO</a> structure containing the list of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">Relative Distinguished Names</a> to be searched.


## -returns



Returns a pointer to the attribute, if one is found. Otherwise, <b>NULL</b> is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindattribute">CertFindAttribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindextension">CertFindExtension</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
 

 

