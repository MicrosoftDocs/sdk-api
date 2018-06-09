---
UID: NF:resapi.ResUtilGetMultiSzValue
title: ResUtilGetMultiSzValue function
author: windows-sdk-content
description: Returns a multiple string value from the cluster database.
old-location: mscs\resutilgetmultiszvalue.htm
old-project: MsCS
ms.assetid: 09547806-16f4-40ce-8713-591a7691a588
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ResUtilGetMultiSzValue, ResUtilGetMultiSzValue function [Failover Cluster], _wolf_resutilgetmultiszvalue, mscs.resutilgetmultiszvalue, resapi/ResUtilGetMultiSzValue
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - ResUtilGetMultiSzValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ResUtilGetMultiSzValue function


## -description


Returns a multiple string value 
    from the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the multiple string value in the cluster database.


### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.


### -param ppszOutValue [out, optional]

Address of the pointer to the retrieved value.


### -param pcbOutValueSize [out]

Pointer to a <b>DWORD</b> in which the size in bytes of the buffer pointed to by 
      <i>ppszOutValue</i> is returned.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error 
       code.




## -remarks



When you are finished with the memory allocated for the value returned by the 
    <b>ResUtilGetMultiSzValue</b> utility function, you must call the function 
    <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release it.




## -see-also




<a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a>



<a href="https://msdn.microsoft.com/d5068cc4-1fdc-430a-a48b-8e024bc20ca3">ResUtilGetBinaryValue</a>



<a href="https://msdn.microsoft.com/2db6126e-a3a7-415b-a436-c3d0748fbc65">ResUtilGetDwordValue</a>



<a href="https://msdn.microsoft.com/c0f1064c-d9ae-43af-9622-beae9aee0ce0">ResUtilGetExpandSzValue</a>



<a href="https://msdn.microsoft.com/c2ba04ea-0f98-4513-b8f8-658056a493e6">ResUtilGetSzValue</a>
 

 

