---
UID: NF:resapi.ResUtilSetExpandSzValue
title: ResUtilSetExpandSzValue function
author: windows-sdk-content
description: Sets an expandable string value in the cluster database. The PRESUTIL_SET_EXPAND_SZ_VALUE type defines a pointer to this function.
old-location: mscs\resutilsetexpandszvalue.htm
tech.root: mscs
ms.assetid: a2049be4-cebb-45bf-b2f7-40841e379b12
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRESUTIL_SET_EXPAND_SZ_VALUE, PRESUTIL_SET_EXPAND_SZ_VALUE function [Failover Cluster], ResUtilSetExpandSzValue, ResUtilSetExpandSzValue function [Failover Cluster], _wolf_resutilsetexpandszvalue, mscs.resutilsetexpandszvalue, resapi/PRESUTIL_SET_EXPAND_SZ_VALUE, resapi/ResUtilSetExpandSzValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ResUtilSetExpandSzValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetExpandSzValue function


## -description


Sets an <a href="e_gly.htm">expandable string</a> value in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>. The <b>PRESUTIL_SET_EXPAND_SZ_VALUE</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the expandable string value in the cluster database.


### -param pszValueName [in]

null-terminated Unicode string containing the name of the value to update.


### -param pszNewValue [in]

Pointer to the new expandable string value.


### -param ppszOutString [in, out, optional]

Pointer to a string pointer that receives a copy of the updated value. If used, callers must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> on *<i>ppszOutValue</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The  <b>ResUtilSetExpandSzValue</b> utility function allocates memory for the new value and calls the  <a href="https://msdn.microsoft.com/865ac74e-5e37-4a2d-a4a4-b23eb45824ce">Cluster API</a> function  <a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>.

An expandable string value contains data that represents a null-terminated Unicode string containing unexpanded references to environment variables such as "%SystemRoot%".

Be sure to call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> on *<i>ppszOutValue</i> to avoid memory leaks.

Do not call  <b>ResUtilSetExpandSzValue</b> from the following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/c7c74440-c98a-4440-8bf4-10ebd1a68608">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<b>ResUtilSetExpandSzValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>



<a href="https://msdn.microsoft.com/6a32169c-af14-40f4-ac45-f9923da544ca">ResUtilSetBinaryValue</a>



<a href="https://msdn.microsoft.com/e8b4393b-84f7-4440-92b5-fd7fa2be96a2">ResUtilSetDwordValue</a>



<a href="https://msdn.microsoft.com/db048ce5-ca83-424b-853f-eda445176c0b">ResUtilSetMultiSzValue</a>



<a href="https://msdn.microsoft.com/b9227df3-0693-4b0f-99de-d10fa3d7acf5">ResUtilSetSzValue</a>
 

 

