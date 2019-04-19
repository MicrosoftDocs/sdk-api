---
UID: NF:resapi.ResUtilGetSzValue
title: ResUtilGetSzValue function (resapi.h)
author: windows-sdk-content
description: Returns a string value from the cluster database.
old-location: mscs\resutilgetszvalue.htm
tech.root: MsCS
ms.assetid: c2ba04ea-0f98-4513-b8f8-658056a493e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_SZ_VALUE, PRESUTIL_GET_SZ_VALUE function [Failover Cluster], ResUtilGetSzValue, ResUtilGetSzValue function [Failover Cluster], _wolf_resutilgetszvalue, mscs.resutilgetszvalue, resapi/PRESUTIL_GET_SZ_VALUE, resapi/ResUtilGetSzValue
ms.topic: function
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
 - ResUtilGetSzValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilGetSzValue function


## -description


Returns a string value from the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the value in the cluster database.


### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to retrieve.


## -returns



If the operation succeeds, 
the function returns a pointer to a buffer containing the string value.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <b>ResUtilGetSzValue</b> utility function allocates the necessary memory for the string parameter value before calling the  <a href="https://msdn.microsoft.com/865ac74e-5e37-4a2d-a4a4-b23eb45824ce">Cluster API</a> function  <a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a> to access the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>. When you are finished with this memory, you must call the function  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release it.

<b>ResUtilGetSzValue</b> also supports expandable and multiple string formats.




## -see-also




<a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a>



<a href="https://msdn.microsoft.com/d5068cc4-1fdc-430a-a48b-8e024bc20ca3">ResUtilGetBinaryValue</a>



<a href="https://msdn.microsoft.com/2db6126e-a3a7-415b-a436-c3d0748fbc65">ResUtilGetDwordValue</a>



<a href="https://msdn.microsoft.com/c0f1064c-d9ae-43af-9622-beae9aee0ce0">ResUtilGetExpandSzValue</a>



<a href="https://msdn.microsoft.com/09547806-16f4-40ce-8713-591a7691a588">ResUtilGetMultiSzValue</a>
 

 

