---
UID: NC:resapi.PRESUTIL_SET_DWORD_VALUE
title: PRESUTIL_SET_DWORD_VALUE
author: windows-sdk-content
description: Sets a numeric value in the cluster database. The PRESUTIL_SET_DWORD_VALUE type defines a pointer to this function.
old-location: mscs\resutilsetdwordvalue.htm
old-project: mscs
ms.assetid: e8b4393b-84f7-4440-92b5-fd7fa2be96a2
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PRESUTIL_SET_DWORD_VALUE, PRESUTIL_SET_DWORD_VALUE callback, PRESUTIL_SET_DWORD_VALUE callback function [Failover Cluster], _wolf_resutilsetdwordvalue, mscs.resutilsetdwordvalue, resapi/PRESUTIL_SET_DWORD_VALUE
ms.prod: windows
ms.technology: windows-sdk
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
 - PRESUTIL_SET_DWORD_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_SET_DWORD_VALUE callback function


## -description


Sets a numeric value in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>. The <b>PRESUTIL_SET_DWORD_VALUE</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the numeric value in the cluster database.


### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to update.


### -param dwNewValue [in]

New <b>DWORD</b> value.


### -param pdwOutValue [in, out]

Optional. Pointer to where the updated value should be copied.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The  <i>ResUtilSetDwordValue</i> utility function updates the cluster database by calling the  <a href="https://msdn.microsoft.com/865ac74e-5e37-4a2d-a4a4-b23eb45824ce">Cluster API</a> function  <a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>.

Do not call  <i>ResUtilSetDwordValue</i> from the following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<i>ResUtilSetDwordValue</i> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>



<a href="https://msdn.microsoft.com/6a32169c-af14-40f4-ac45-f9923da544ca">ResUtilSetBinaryValue</a>



<a href="https://msdn.microsoft.com/a2049be4-cebb-45bf-b2f7-40841e379b12">ResUtilSetExpandSzValue</a>



<a href="https://msdn.microsoft.com/db048ce5-ca83-424b-853f-eda445176c0b">ResUtilSetMultiSzValue</a>



<a href="https://msdn.microsoft.com/b9227df3-0693-4b0f-99de-d10fa3d7acf5">ResUtilSetSzValue</a>
 

 

