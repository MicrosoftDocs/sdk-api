---
UID: NC:resapi.PCLOSE_CLUSTER_CRYPT_PROVIDER
title: PCLOSE_CLUSTER_CRYPT_PROVIDER
author: windows-driver-content
description: Closes a handle to a Cryptographic Service Provider (CSP). The PCLOSE_CLUSTER_CRYPT_PROVIDER type defines a pointer to this function.
old-location: mscs\closeclustercryptprovider.htm
old-project: MsCS
ms.assetid: 844D991A-6B29-4ADE-8CFE-114FD4AF7C9B
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLOSE_CLUSTER_CRYPT_PROVIDER, PCLOSE_CLUSTER_CRYPT_PROVIDER callback function [Failover Cluster], mscs.closeclustercryptprovider, resapi/PCLOSE_CLUSTER_CRYPT_PROVIDER
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
-	PCLOSE_CLUSTER_CRYPT_PROVIDER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PCLOSE_CLUSTER_CRYPT_PROVIDER callback


## -description


Closes a handle to a Cryptographic Service Provider (CSP). The <b>PCLOSE_CLUSTER_CRYPT_PROVIDER</b> type defines a pointer to this function.


## -parameters




### -param hClusCryptProvider [in]

A <a href="https://msdn.microsoft.com/B1933FA5-CED7-4C11-880E-FC0BAD5DDE45">HCLUSCRYPTPROVIDER</a> structure that contains a handle to a CSP.


## -returns



If the operation completes successfully, this function returns <b>ERROR_SUCCESS</b>; otherwise, it returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/74677418-CA63-4B4E-9844-A3A47AFFAD49">Cryptography Functions</a>



<a href="https://msdn.microsoft.com/DFD5C0F1-07BF-4339-8B35-2918B32F66B3">OpenClusterCryptProvider</a>
 

 

