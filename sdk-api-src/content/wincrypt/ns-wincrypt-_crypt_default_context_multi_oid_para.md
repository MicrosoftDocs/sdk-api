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

# _CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure


## -description


The <b>CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA</b> structure is used with the <a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a> function to contain an array of object identifier strings.


## -struct-fields




### -field cOID

The number of elements in the <b>rgpszOID</b> array.


### -field rgpszOID

An array of pointers to null-terminated ANSI strings that contain the object identifier strings of the certificate signature algorithm to install the default provider for, for example, <b>szOID_OIWSEC_md5RSA</b>. The <b>cOID</b> member of this structure contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a>
 

 

