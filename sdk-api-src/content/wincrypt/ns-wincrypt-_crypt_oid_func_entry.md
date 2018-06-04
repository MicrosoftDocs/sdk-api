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

# _CRYPT_OID_FUNC_ENTRY structure


## -description


The <b>CRYPT_OID_FUNC_ENTRY</b> structure contains an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a pointer to its related function. It is used with 
<a href="https://msdn.microsoft.com/934e8278-0e0b-4402-a2b6-ff1e913d54c9">CryptInstallOIDFunctionAddress</a>.


## -struct-fields




### -field pszOID

If the high-order word of the OID is nonzero, <b>pszOID</b> is a pointer to either an OID string, such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string, such as "file". If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier.


### -field pvFuncAddr

The starting address of the function that the OID identifies.


## -see-also




<a href="https://msdn.microsoft.com/934e8278-0e0b-4402-a2b6-ff1e913d54c9">CryptInstallOIDFunctionAddress</a>
 

 

