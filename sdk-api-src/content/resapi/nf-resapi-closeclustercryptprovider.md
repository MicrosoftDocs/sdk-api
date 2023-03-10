---
UID: NF:resapi.CloseClusterCryptProvider
title: CloseClusterCryptProvider function (resapi.h)
description: Closes a handle to a Cryptographic Service Provider (CSP). The PCLOSE_CLUSTER_CRYPT_PROVIDER type defines a pointer to this function.
helpviewer_keywords: ["CloseClusterCryptProvider","CloseClusterCryptProvider function [Failover Cluster]","PCLOSE_CLUSTER_CRYPT_PROVIDER","PCLOSE_CLUSTER_CRYPT_PROVIDER function [Failover Cluster]","mscs.closeclustercryptprovider","resapi/CloseClusterCryptProvider","resapi/PCLOSE_CLUSTER_CRYPT_PROVIDER"]
old-location: mscs\closeclustercryptprovider.htm
tech.root: MsCS
ms.assetid: 844D991A-6B29-4ADE-8CFE-114FD4AF7C9B
ms.date: 12/05/2018
ms.keywords: CloseClusterCryptProvider, CloseClusterCryptProvider function [Failover Cluster], PCLOSE_CLUSTER_CRYPT_PROVIDER, PCLOSE_CLUSTER_CRYPT_PROVIDER function [Failover Cluster], mscs.closeclustercryptprovider, resapi/CloseClusterCryptProvider, resapi/PCLOSE_CLUSTER_CRYPT_PROVIDER
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
 - CloseClusterCryptProvider
 - resapi/CloseClusterCryptProvider
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
 - CloseClusterCryptProvider
---

# CloseClusterCryptProvider function


## -description

Closes a handle to a Cryptographic Service Provider (CSP). The <b>PCLOSE_CLUSTER_CRYPT_PROVIDER</b> type defines a pointer to this function.

## -parameters

### -param hClusCryptProvider [in]

A <a href="/previous-versions/windows/desktop/legacy/dn823545(v=vs.85)">HCLUSCRYPTPROVIDER</a> structure that contains a handle to a CSP.

## -returns

If the operation completes successfully, this function returns <b>ERROR_SUCCESS</b>; otherwise, it returns a system error code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cryptography-functions">Cryptography Functions</a>



<a href="/windows/desktop/api/resapi/nf-resapi-openclustercryptprovider">OpenClusterCryptProvider</a>