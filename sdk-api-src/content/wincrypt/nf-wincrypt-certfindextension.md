---
UID: NF:wincrypt.CertFindExtension
title: CertFindExtension function
author: windows-sdk-content
description: The CertFindExtension function finds the first extension in the CERT_EXTENSION array, as identified by its object identifier (OID).
old-location: security\certfindextension.htm
tech.root: seccrypto
ms.assetid: 489c58b6-a704-4f54-bc64-34eacafc347c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CertFindExtension, CertFindExtension function [Security], _crypto2_certfindextension, security.certfindextension, wincrypt/CertFindExtension
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
 - CertFindExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFindExtension function


## -description


The <b>CertFindExtension</b> function finds the first extension in the 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> array, as identified by its <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This function can be used in the processing of a decoded certificate. A 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure is derived from a decoded certificate. The <b>CERT_INFO</b> structure's <b>rgExtension</b> member is  passed to <b>CertFindExtension</b> in the <i>rgExtensions</i> parameter. This function determines whether a particular extension is in the array, and if so, returns a pointer to it


## -parameters




### -param pszObjId [in]

A pointer to the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) to use in the search.


### -param cExtensions [in]

Number of extensions in the <i>rgExtensions</i> array.


### -param rgExtensions [in]

Array of 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures.


## -returns



Returns a pointer to the extension, if one is found. Otherwise, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/99d690fb-ea85-4cb1-9fb0-bdb02e4ac50a">CertFindAttribute</a>



<a href="https://msdn.microsoft.com/31f82a02-e90a-48de-857a-9fbb03048b5c">CertFindRDNAttr</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

