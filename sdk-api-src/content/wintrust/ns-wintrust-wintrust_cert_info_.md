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

# WINTRUST_CERT_INFO_ structure


## -description


<p class="CCE_Message">[The  <b>WINTRUST_CERT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_CERT_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>.


## -struct-fields




### -field cbStruct

Count of bytes in this structure.


### -field pcwszDisplayName

String with the name of the memory object pointed to by the <b>pbMem</b> member of the 
<a href="https://msdn.microsoft.com/8b13d355-4d24-4d8e-aae3-db16467999be">WINTRUST_BLOB_INFO</a> structure.


### -field psCertContext

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> to be verified.


### -field chStores

The number of store handles in <b>pahStores</b>.


### -field pahStores

An array of open <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a> to add to the list of stores that the policy provider looks in to find certificates while building a trust chain.


### -field dwFlags

 


### -field psftVerifyAsOf

 



