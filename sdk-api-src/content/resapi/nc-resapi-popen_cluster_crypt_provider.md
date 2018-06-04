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

# POPEN_CLUSTER_CRYPT_PROVIDER callback function


## -description


Opens a handle to a Cryptographic Service Provider (CSP) in order to manage the encryption of <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a> data for a cluster resource. The <b>POPEN_CLUSTER_CRYPT_PROVIDER</b> type defines a pointer to this function.


## -parameters




### -param lpszResource [in]

A pointer to a null-terminated Unicode string that contains the name of the cluster resource that is associated with the <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a> data.


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



If the operation completes successfully, this function returns a <a href="https://msdn.microsoft.com/B1933FA5-CED7-4C11-880E-FC0BAD5DDE45">HCLUSCRYPTPROVIDER</a> structure containing a handle to the CSP.




## -see-also




<a href="https://msdn.microsoft.com/844D991A-6B29-4ADE-8CFE-114FD4AF7C9B">CloseClusterCryptProvider</a>



<a href="https://msdn.microsoft.com/74677418-CA63-4B4E-9844-A3A47AFFAD49">Cryptography Functions</a>
 

 

