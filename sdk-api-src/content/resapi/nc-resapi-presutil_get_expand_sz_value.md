---
UID: NC:resapi.PRESUTIL_GET_EXPAND_SZ_VALUE
title: PRESUTIL_GET_EXPAND_SZ_VALUE
author: windows-sdk-content
description: Returns a expandable string value from the cluster database.
old-location: mscs\resutilgetexpandszvalue.htm
old-project: mscs
ms.assetid: c0f1064c-d9ae-43af-9622-beae9aee0ce0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRESUTIL_GET_EXPAND_SZ_VALUE, PRESUTIL_GET_EXPAND_SZ_VALUE callback, PRESUTIL_GET_EXPAND_SZ_VALUE callback function [Failover Cluster], _wolf_resutilgetexpandszvalue, mscs.resutilgetexpandszvalue, resapi/PRESUTIL_GET_EXPAND_SZ_VALUE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_GET_EXPAND_SZ_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_GET_EXPAND_SZ_VALUE callback function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2003. This function is not exported 
    from ResUtils.dll and programs or DLLs that statically link to it will not load.]

Returns a <a href="e_gly.htm">expandable string</a> value from the 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the expandable string value in the cluster database.


### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.


### -param bExpand [in]

If <b>TRUE</b>, the function expands the string before returning. If 
       <b>FALSE</b>, the string is returned in an expandable form.


## -returns



If the operations succeeds, the function returns a null-terminated Unicode string containing a copy of the 
       specified value.

If the operation fails, the function returns <b>NULL</b>. For more information, see 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When you are finished with the memory allocated for the value returned by the 
     <i>ResUtilGetExpandSzValue</i> utility function, you 
     must call the function <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release it.




## -see-also




<a href="https://msdn.microsoft.com/78ea27da-2b95-46df-b01e-4a3717276859">ClusterRegQueryValue</a>



<a href="https://msdn.microsoft.com/d5068cc4-1fdc-430a-a48b-8e024bc20ca3">ResUtilGetBinaryValue</a>



<a href="https://msdn.microsoft.com/2db6126e-a3a7-415b-a436-c3d0748fbc65">ResUtilGetDwordValue</a>



<a href="https://msdn.microsoft.com/09547806-16f4-40ce-8713-591a7691a588">ResUtilGetMultiSzValue</a>



<a href="https://msdn.microsoft.com/c2ba04ea-0f98-4513-b8f8-658056a493e6">ResUtilGetSzValue</a>
 

 

