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

# CertFreeServerOcspResponseContext function


## -description


The <b>CertFreeServerOcspResponseContext</b> function decrements the reference count for a <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure. If the reference count becomes zero, memory allocated for the structure is released.


## -parameters




### -param pServerOcspResponseContext [in]

A pointer to a <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure that contains a value returned by the <a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a> function.


## -returns



This function has no return value.



