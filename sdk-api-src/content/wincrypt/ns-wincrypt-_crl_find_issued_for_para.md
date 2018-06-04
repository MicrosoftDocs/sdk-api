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

# _CRL_FIND_ISSUED_FOR_PARA structure


## -description


The <b>CRL_FIND_ISSUED_FOR_PARA</b> structure contains the certificate contexts of both a subject and a certificate issuer. For more information, see 
<a href="https://msdn.microsoft.com/3e481912-204a-4d86-ab67-81f8ae4d1aaa">CertFindCRLInStore</a>.


## -struct-fields




### -field pSubjectCert

A pointer to a subject's certificate context.


### -field pIssuerCert

A pointer to a certificate issuer's certificate context.

