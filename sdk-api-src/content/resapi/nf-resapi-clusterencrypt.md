---
UID: NF:resapi.ClusterEncrypt
title: ClusterEncrypt function (resapi.h)
description: Encrypts Checkpointing data for a Cryptographic Service Provider (CSP).
helpviewer_keywords: ["ClusterEncrypt","ClusterEncrypt function [Failover Cluster]","PCLUSTER_ENCRYPT","PCLUSTER_ENCRYPT function [Failover Cluster]","mscs.clusterencrypt","resapi/ClusterEncrypt","resapi/PCLUSTER_ENCRYPT"]
old-location: mscs\clusterencrypt.htm
tech.root: MsCS
ms.assetid: 5C15E553-D6C6-47F7-B6DE-E7CA4795CA87
ms.date: 12/05/2018
ms.keywords: ClusterEncrypt, ClusterEncrypt function [Failover Cluster], PCLUSTER_ENCRYPT, PCLUSTER_ENCRYPT function [Failover Cluster], mscs.clusterencrypt, resapi/ClusterEncrypt, resapi/PCLUSTER_ENCRYPT
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterEncrypt
 - resapi/ClusterEncrypt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ClusterEncrypt
---

# ClusterEncrypt function


## -description

Encrypts <a href="/previous-versions/windows/desktop/mscs/checkpointing">Checkpointing</a> data for a Cryptographic Service Provider (CSP).

## -parameters

### -param hClusCryptProvider [in]

A <a href="/previous-versions/windows/desktop/legacy/dn823545(v=vs.85)">HCLUSCRYPTPROVIDER</a> structure that contains a handle to the CSP.

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

<a href="/previous-versions/windows/desktop/mscs/cryptography-functions">Cryptography Functions</a>