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

# _CERT_CREATE_CONTEXT_PARA structure


## -description


The <b>CERT_CREATE_CONTEXT_PARA</b> structure defines additional values that can be used when calling the <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> function.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pfnFree

A pointer to the function that  frees the <i>pbEncoded</i> parameter of the <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> function. The  <b>pfnFree</b> function is called when the context created by  <b>CertCreateContext</b> is freed. This value can be <b>NULL</b>, in which case the <i>pbEncoded</i> parameter of the <b>CertCreateContext</b> function is not freed.


### -field pvFree

The address of the memory that gets freed by the <b>pfnFree</b> function. If <b>pvFree</b> is <b>NULL</b>, then the <i>pbEncoded</i> parameter of the <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> function is freed.


### -field pfnSort

A <a href="https://msdn.microsoft.com/5ad79970-d076-4e97-bf56-d6aad4b46eaa">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a> function pointer that will be called for each sorted context entry.

This member is only present for a <b>CERT_STORE_CTL_CONTEXT</b> when the <b>CERT_CREATE_CONTEXT_SORTED_FLAG</b> flag is set in the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> function. You must verify that this member is present before trying to access it by examining the <b>cbSize</b> member of this structure.


### -field pvSort

An application-defined value that will be passed in the <i>pvSort</i> parameter of the <a href="https://msdn.microsoft.com/5ad79970-d076-4e97-bf56-d6aad4b46eaa">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a> callback function.

This member is only present for a <b>CERT_STORE_CTL_CONTEXT</b> when the <b>CERT_CREATE_CONTEXT_SORTED_FLAG</b> flag is set in the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a> function. You must verify that this member is present before trying to access it by examining the <b>cbSize</b> member of this structure.


## -see-also




<a href="https://msdn.microsoft.com/0911054b-a47a-4046-b121-a236fc4b018b">CertCreateContext</a>



<a href="https://msdn.microsoft.com/5ad79970-d076-4e97-bf56-d6aad4b46eaa">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a>
 

 

