---
UID: NC:resapi.PRESUTIL_GET_BINARY_VALUE
title: PRESUTIL_GET_BINARY_VALUE
author: windows-driver-content
description: Returns a binary value from the cluster database.
old-location: mscs\resutilgetbinaryvalue.htm
old-project: MsCS
ms.assetid: d5068cc4-1fdc-430a-a48b-8e024bc20ca3
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_GET_BINARY_VALUE, PRESUTIL_GET_BINARY_VALUE callback, PRESUTIL_GET_BINARY_VALUE callback function [Failover Cluster], _wolf_resutilgetbinaryvalue, mscs.resutilgetbinaryvalue, resapi/PRESUTIL_GET_BINARY_VALUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
-	PRESUTIL_GET_BINARY_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_GET_BINARY_VALUE callback function


## -description


Returns a binary value from the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key in the cluster database that identifies the location of the value to retrieve.


### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.


### -param *ppbOutValue [out, optional]

Address of the pointer to the retrieved value.


### -param pcbOutValueSize [out]

Pointer to a <b>DWORD</b> in which the size in bytes of the buffer pointed to by <i>ppbOutValue</i> is returned.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The  <i>ResUtilGetBinaryValue</i> utility function takes care of allocating the necessary memory for the value and then calls the  <a href="https://msdn.microsoft.com/865ac74e-5e37-4a2d-a4a4-b23eb45824ce">Cluster API</a> function  <a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a>. When you are finished with the allocated memory, you must call the function  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release it.




## -see-also




<a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a>



<a href="https://msdn.microsoft.com/2db6126e-a3a7-415b-a436-c3d0748fbc65">ResUtilGetDwordValue</a>



<a href="https://msdn.microsoft.com/c0f1064c-d9ae-43af-9622-beae9aee0ce0">ResUtilGetExpandSzValue</a>



<a href="https://msdn.microsoft.com/09547806-16f4-40ce-8713-591a7691a588">ResUtilGetMultiSzValue</a>



<a href="https://msdn.microsoft.com/c2ba04ea-0f98-4513-b8f8-658056a493e6">ResUtilGetSzValue</a>
 

 

