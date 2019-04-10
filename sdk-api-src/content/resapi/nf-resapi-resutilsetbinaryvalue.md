---
UID: NF:resapi.ResUtilSetBinaryValue
title: ResUtilSetBinaryValue function (resapi.h)
author: windows-sdk-content
description: Sets a binary value in the cluster database.
old-location: mscs\resutilsetbinaryvalue.htm
tech.root: MsCS
ms.assetid: 6a32169c-af14-40f4-ac45-f9923da544ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_BINARY_VALUE, PRESUTIL_SET_BINARY_VALUE function [Failover Cluster], ResUtilSetBinaryValue, ResUtilSetBinaryValue function [Failover Cluster], _wolf_resutilsetbinaryvalue, mscs.resutilsetbinaryvalue, resapi/PRESUTIL_SET_BINARY_VALUE, resapi/ResUtilSetBinaryValue
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
 - ResUtilSetBinaryValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetBinaryValue function


## -description


Sets a binary value in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the binary value in the cluster database.


### -param pszValueName [in]

A null-terminated Unicode string containing the name of the value to update.


### -param pbNewValue [in]

Pointer to the new binary value.


### -param cbNewValueSize [in]

Size of the new binary value.


### -param ppbOutValue [in, out, optional]

Address of a pointer to the new binary value.


### -param pcbOutValueSize [in, out]

Pointer to a <b>DWORD</b> in which the size in bytes of the value pointed to by <i>ppbOutValue</i> is returned.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
</table>
 




## -remarks



The  <b>ResUtilSetBinaryValue</b> utility function allocates memory for the <i>ppbOutValue</i> pointer using the function  <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>, calls the  <a href="https://msdn.microsoft.com/865ac74e-5e37-4a2d-a4a4-b23eb45824ce">Cluster API</a> function  <a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>, and then copies the new value to this buffer. If the pointer is not <b>NULL</b>,  <b>ResUtilSetBinaryValue</b> also deallocates it. As callers of this function, you are responsible for deallocating the buffer using the function  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.

Do not call  <b>ResUtilSetBinaryValue</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetBinaryValue</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/6e4fee56-1c18-4f6d-81ae-c305aae59572">ClusterRegSetValue</a>



<a href="https://msdn.microsoft.com/e8b4393b-84f7-4440-92b5-fd7fa2be96a2">ResUtilSetDwordValue</a>



<a href="https://msdn.microsoft.com/a2049be4-cebb-45bf-b2f7-40841e379b12">ResUtilSetExpandSzValue</a>



<a href="https://msdn.microsoft.com/db048ce5-ca83-424b-853f-eda445176c0b">ResUtilSetMultiSzValue</a>



<a href="https://msdn.microsoft.com/b9227df3-0693-4b0f-99de-d10fa3d7acf5">ResUtilSetSzValue</a>
 

 

