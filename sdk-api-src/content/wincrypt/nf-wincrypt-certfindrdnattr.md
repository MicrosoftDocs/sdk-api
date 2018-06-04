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
 

 

