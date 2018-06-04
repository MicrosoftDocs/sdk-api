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

# PstGetCertificates function


## -description


Retrieves certificate chains that specify certificates that can be used to authenticate a user on the specified server.


## -parameters




### -param pTargetName [in]

The name of the server to check.


### -param cCriteria [in]

The number of elements in the <i>rgpCriteria</i> array.


### -param rgpCriteria [in, optional]

A constant pointer to an array of <a href="https://msdn.microsoft.com/246722a9-5db6-4a82-8f29-f60f0a2263e3">CERT_SELECT_CRITERIA</a> structures that specify the criteria used to select certificate chains.


### -param bIsClient [in]

<b>TRUE</b> if the caller is the client; otherwise, <b>FALSE</b>.


### -param pdwCertChainContextCount [out]

The number of elements in the <i>ppCertChainContexts</i> array.


### -param ppCertChainContexts [out]

The address of a pointer to an array of <a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> structures that specifies the certificate chains of certificates that can be used to authenticate a user on the server specified by the <i>pTargetName</i> parameter.


## -returns



If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



