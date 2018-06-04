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
 

 

