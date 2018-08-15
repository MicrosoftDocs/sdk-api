---
UID: NF:resapi.CloseClusterCryptProvider
title: CloseClusterCryptProvider function
author: windows-sdk-content
description: Closes a handle to a Cryptographic Service Provider (CSP). The PCLOSE_CLUSTER_CRYPT_PROVIDER type defines a pointer to this function.
old-location: mscs\closeclustercryptprovider.htm
old-project: mscs
ms.assetid: 844D991A-6B29-4ADE-8CFE-114FD4AF7C9B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CloseClusterCryptProvider, CloseClusterCryptProvider function [Failover Cluster], PCLOSE_CLUSTER_CRYPT_PROVIDER, PCLOSE_CLUSTER_CRYPT_PROVIDER function [Failover Cluster], mscs.closeclustercryptprovider, resapi/CloseClusterCryptProvider, resapi/PCLOSE_CLUSTER_CRYPT_PROVIDER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - CloseClusterCryptProvider
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
---

# CloseClusterCryptProvider function


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
 

 

