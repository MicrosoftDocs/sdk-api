---
UID: NF:resapi.ClusterEncrypt
title: ClusterEncrypt function
author: windows-sdk-content
description: Encrypts Checkpointing data for a Cryptographic Service Provider (CSP).
old-location: mscs\clusterencrypt.htm
tech.root: mscs
ms.assetid: 5C15E553-D6C6-47F7-B6DE-E7CA4795CA87
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ClusterEncrypt, ClusterEncrypt function [Failover Cluster], PCLUSTER_ENCRYPT, PCLUSTER_ENCRYPT function [Failover Cluster], mscs.clusterencrypt, resapi/ClusterEncrypt, resapi/PCLUSTER_ENCRYPT
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
 - ClusterEncrypt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterEncrypt function


## -description


Encrypts <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a> data for a Cryptographic Service Provider (CSP).


## -parameters




### -param hClusCryptProvider [in]

A <a href="https://msdn.microsoft.com/B1933FA5-CED7-4C11-880E-FC0BAD5DDE45">HCLUSCRYPTPROVIDER</a> structure that contains a handle to the CSP.


### -param pData [in]

A pointer to the data to encrypt.


### -param cbData [in]

The total number of bytes in the data pointed to by the <i>pDta</i> parameter.


### -param ppData [out]

A pointer to a buffer that receives the encrypted data.


### -param pcbData [out]

The total number of bytes in the data pointed to by the <i>pcbData</i> parameter.


## -returns



If the operation completes successfully, this function returns <b>ERROR_SUCCESS</b>; otherwise, it returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/74677418-CA63-4B4E-9844-A3A47AFFAD49">Cryptography Functions</a>
 

 

