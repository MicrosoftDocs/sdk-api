---
UID: NF:resapi.ClusterDecrypt
title: ClusterDecrypt function
author: windows-sdk-content
description: Decrypts Checkpointing data for a Cryptographic Service Provider (CSP).
old-location: mscs\clusterdecrypt.htm
tech.root: mscs
ms.assetid: F851BA13-3261-462C-98EA-402F77A39A14
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ClusterDecrypt, ClusterDecrypt function [Failover Cluster], PCLUSTER_DECRYPT, PCLUSTER_DECRYPT function [Failover Cluster], mscs.clusterdecrypt, resapi/ClusterDecrypt, resapi/PCLUSTER_DECRYPT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ClusterDecrypt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterDecrypt function


## -description


Decrypts <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a> data for a Cryptographic Service Provider (CSP).


## -parameters




### -param hClusCryptProvider [in]

A <a href="https://msdn.microsoft.com/B1933FA5-CED7-4C11-880E-FC0BAD5DDE45">HCLUSCRYPTPROVIDER</a> structure that contains a handle to the CSP.


### -param pCryptInput [in]

A pointer to the data to decrypt.


### -param cbCryptInput [in]

The total number of bytes in the data pointed to by the <i>pCryptInput</i> parameter.


### -param ppCryptOutput [out]

A pointer to a buffer that receives the decrypted data.


### -param pcbCryptOutput [out]

The total number of bytes in the data pointed to by the <i>ppCryptOutput</i> parameter.


## -returns



If the operation completes successfully, this function returns <b>ERROR_SUCCESS</b>; otherwise, it returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/74677418-CA63-4B4E-9844-A3A47AFFAD49">Cryptography Functions</a>
 

 

