---
UID: NC:resapi.PCLUSTER_DECRYPT
title: PCLUSTER_DECRYPT
author: windows-driver-content
description: Decrypts Checkpointing data for a Cryptographic Service Provider (CSP).
old-location: mscs\clusterdecrypt.htm
old-project: MsCS
ms.assetid: F851BA13-3261-462C-98EA-402F77A39A14
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSTER_DECRYPT, PCLUSTER_DECRYPT callback function [Failover Cluster], mscs.clusterdecrypt, resapi/PCLUSTER_DECRYPT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PCLUSTER_DECRYPT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PCLUSTER_DECRYPT callback


## -description


Decrypts <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a> data for a Cryptographic Service Provider (CSP).


## -parameters




### -param hClusCryptProvider [in]

A <a href="https://msdn.microsoft.com/B1933FA5-CED7-4C11-880E-FC0BAD5DDE45">HCLUSCRYPTPROVIDER</a> structure that contains a handle to the CSP.


### -param pCryptInput [in]

A pointer to the data to decrypt.


### -param cbCryptInput [in]

The total number of bytes in the data pointed to by the <i>pCryptInput</i> parameter.


### -param *ppCryptOutput [out]

A pointer to a buffer that receives the decrypted data.


### -param pcbCryptOutput [out]

The total number of bytes in the data pointed to by the <i>ppCryptOutput</i> parameter.


## -returns



If the operation completes successfully, this function returns <b>ERROR_SUCCESS</b>; otherwise, it returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/74677418-CA63-4B4E-9844-A3A47AFFAD49">Cryptography Functions</a>
 

 

