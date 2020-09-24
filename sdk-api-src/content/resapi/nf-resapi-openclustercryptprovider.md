---
UID: NF:resapi.OpenClusterCryptProvider
title: OpenClusterCryptProvider function (resapi.h)
description: Opens a handle to a Cryptographic Service Provider (CSP) in order to manage the encryption of Checkpointing data for a cluster resource. The POPEN_CLUSTER_CRYPT_PROVIDER type defines a pointer to this function.
helpviewer_keywords: ["OpenClusterCryptProvider","OpenClusterCryptProvider function [Failover Cluster]","POPEN_CLUSTER_CRYPT_PROVIDER","POPEN_CLUSTER_CRYPT_PROVIDER function [Failover Cluster]","PROV_DH_SCHANNEL","PROV_DSS","PROV_DSS_DH","PROV_EC_ECDSA_FULL","PROV_EC_ECDSA_SIG","PROV_EC_ECNRA_FULL","PROV_EC_ECNRA_SIG","PROV_FORTEZZA","PROV_INTEL_SEC","PROV_MS_EXCHANGE","PROV_REPLACE_OWF","PROV_RNG","PROV_RSA_AES","PROV_RSA_FULL","PROV_RSA_SCHANNEL","PROV_RSA_SIG","PROV_SPYRUS_LYNKS","PROV_SSL","mscs.openclustercryptprovider","resapi/OpenClusterCryptProvider","resapi/POPEN_CLUSTER_CRYPT_PROVIDER"]
old-location: mscs\openclustercryptprovider.htm
tech.root: MsCS
ms.assetid: DFD5C0F1-07BF-4339-8B35-2918B32F66B3
ms.date: 12/05/2018
ms.keywords: OpenClusterCryptProvider, OpenClusterCryptProvider function [Failover Cluster], POPEN_CLUSTER_CRYPT_PROVIDER, POPEN_CLUSTER_CRYPT_PROVIDER function [Failover Cluster], PROV_DH_SCHANNEL, PROV_DSS, PROV_DSS_DH, PROV_EC_ECDSA_FULL, PROV_EC_ECDSA_SIG, PROV_EC_ECNRA_FULL, PROV_EC_ECNRA_SIG, PROV_FORTEZZA, PROV_INTEL_SEC, PROV_MS_EXCHANGE, PROV_REPLACE_OWF, PROV_RNG, PROV_RSA_AES, PROV_RSA_FULL, PROV_RSA_SCHANNEL, PROV_RSA_SIG, PROV_SPYRUS_LYNKS, PROV_SSL, mscs.openclustercryptprovider, resapi/OpenClusterCryptProvider, resapi/POPEN_CLUSTER_CRYPT_PROVIDER
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
 - OpenClusterCryptProvider
 - resapi/OpenClusterCryptProvider
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
 - OpenClusterCryptProvider
---

# OpenClusterCryptProvider function


## -description

Opens a handle to a Cryptographic Service Provider (CSP) in order to manage the encryption of <a href="/previous-versions/windows/desktop/mscs/checkpointing">Checkpointing</a> data for a cluster resource. The <b>POPEN_CLUSTER_CRYPT_PROVIDER</b> type defines a pointer to this function.

## -parameters

### -param lpszResource [in]

A pointer to a null-terminated Unicode string that contains the name of the cluster resource that is associated with the <a href="/previous-versions/windows/desktop/mscs/checkpointing">Checkpointing</a> data.

### -param lpszProvider [in]

A pointer to a null-terminated Unicode string that contains the name of the CSP.

### -param dwType [in]

A bitmask that specifies the CSP type.


This parameter can be set to one of the following values:





#### PROV_RSA_FULL (1)



#### PROV_RSA_SIG (2)



#### PROV_DSS (3)



#### PROV_FORTEZZA (4)



#### PROV_MS_EXCHANGE (5)



#### PROV_SSL (6)



#### PROV_RSA_SCHANNEL (12)



#### PROV_DSS_DH (13)



#### PROV_EC_ECDSA_SIG (14)



#### PROV_EC_ECNRA_SIG (15)



#### PROV_EC_ECDSA_FULL (16)



#### PROV_EC_ECNRA_FULL (17)



#### PROV_DH_SCHANNEL (18)



#### PROV_SPYRUS_LYNKS (20)



#### PROV_RNG (21)



#### PROV_INTEL_SEC (22)



#### PROV_REPLACE_OWF (23)



#### PROV_RSA_AES (24)

### -param dwFlags [in]

The flags that specify the settings for the operation. This parameter can be set to the default value "0", or <b>CLUS_CREATE_CRYPT_CONTAINER_NOT_FOUND</b> (0x0001).

## -returns

If the operation completes successfully, this function returns a <a href="/previous-versions/windows/desktop/legacy/dn823545(v=vs.85)">HCLUSCRYPTPROVIDER</a> structure containing a handle to the CSP.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-closeclustercryptprovider">CloseClusterCryptProvider</a>



<a href="/previous-versions/windows/desktop/mscs/cryptography-functions">Cryptography Functions</a>