---
UID: NF:resapi.ClusterDecrypt
title: ClusterDecrypt function (resapi.h)
description: Decrypts Checkpointing data for a Cryptographic Service Provider (CSP).
helpviewer_keywords: ["ClusterDecrypt","ClusterDecrypt function [Failover Cluster]","PCLUSTER_DECRYPT","PCLUSTER_DECRYPT function [Failover Cluster]","mscs.clusterdecrypt","resapi/ClusterDecrypt","resapi/PCLUSTER_DECRYPT"]
old-location: mscs\clusterdecrypt.htm
tech.root: MsCS
ms.assetid: F851BA13-3261-462C-98EA-402F77A39A14
ms.date: 12/05/2018
ms.keywords: ClusterDecrypt, ClusterDecrypt function [Failover Cluster], PCLUSTER_DECRYPT, PCLUSTER_DECRYPT function [Failover Cluster], mscs.clusterdecrypt, resapi/ClusterDecrypt, resapi/PCLUSTER_DECRYPT
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
 - ClusterDecrypt
 - resapi/ClusterDecrypt
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
 - ClusterDecrypt
---

# ClusterDecrypt function


## -description

Decrypts <a href="/previous-versions/windows/desktop/mscs/checkpointing">Checkpointing</a> data for a Cryptographic Service Provider (CSP).

## -parameters

### -param hClusCryptProvider [in]

A <a href="/previous-versions/windows/desktop/legacy/dn823545(v=vs.85)">HCLUSCRYPTPROVIDER</a> structure that contains a handle to the CSP.

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

<a href="/previous-versions/windows/desktop/mscs/cryptography-functions">Cryptography Functions</a>