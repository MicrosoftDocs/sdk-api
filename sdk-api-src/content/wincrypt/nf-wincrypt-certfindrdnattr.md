---
UID: NF:wincrypt.CertFindRDNAttr
title: CertFindRDNAttr function
author: windows-sdk-content
description: The CertFindRDNAttr function finds the first RDN attribute identified by its object identifier (OID) in a list of the Relative Distinguished Names (RDN).
old-location: security\certfindrdnattr.htm
tech.root: seccrypto
ms.assetid: 31f82a02-e90a-48de-857a-9fbb03048b5c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CertFindRDNAttr, CertFindRDNAttr function [Security], _crypto2_certfindrdnattr, security.certfindrdnattr, wincrypt/CertFindRDNAttr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFindRDNAttr function


## -description


The <b>CertFindRDNAttr</b> function finds the first <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RDN</a> attribute identified by its <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) in a list of the <i>Relative Distinguished Names</i> (RDN).


## -parameters




### -param pszObjId [in]

A pointer to the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) to use In the search.


### -param pName [in]

A pointer to a 
<a href="https://msdn.microsoft.com/402d1051-d91a-4a79-96f6-10ed96a32d5c">CERT_NAME_INFO</a> structure containing the list of the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">Relative Distinguished Names</a> to be searched.


## -returns



Returns a pointer to the attribute, if one is found. Otherwise, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/99d690fb-ea85-4cb1-9fb0-bdb02e4ac50a">CertFindAttribute</a>



<a href="https://msdn.microsoft.com/489c58b6-a704-4f54-bc64-34eacafc347c">CertFindExtension</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

