---
UID: NF:wincrypt.CertFindAttribute
title: CertFindAttribute function
author: windows-sdk-content
description: The CertFindAttribute function finds the first attribute in the CRYPT_ATTRIBUTE array, as identified by its object identifier (OID).
old-location: security\certfindattribute.htm
tech.root: seccrypto
ms.assetid: 99d690fb-ea85-4cb1-9fb0-bdb02e4ac50a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CertFindAttribute, CertFindAttribute function [Security], _crypto2_certfindattribute, security.certfindattribute, wincrypt/CertFindAttribute
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
 - CertFindAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFindAttribute function


## -description


The <b>CertFindAttribute</b> function finds the first attribute in the 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> array, as identified by its <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This function can be used in the processing of a decoded <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. A 
<a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a> structure is derived from a decoded certificate request. The <b>rgAttribute</b> array is retrieved from that structure and passed to this function in the <i>rgAttr</i> parameter. This function determines whether a particular attribute is in the array, and if so, returns a pointer to it.


## -parameters




### -param pszObjId [in]

A pointer to the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) to use in the search.


### -param cAttr [in]

Number of attributes in the <i>rgAttr</i> array.


### -param rgAttr [in]

Array of 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures.


## -returns



Returns a pointer to the attribute, if one is found. Otherwise, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/489c58b6-a704-4f54-bc64-34eacafc347c">CertFindExtension</a>



<a href="https://msdn.microsoft.com/31f82a02-e90a-48de-857a-9fbb03048b5c">CertFindRDNAttr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

