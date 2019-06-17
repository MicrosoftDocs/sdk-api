---
UID: NF:resapi.ResUtilGetBinaryValue
title: ResUtilGetBinaryValue function (resapi.h)
author: windows-sdk-content
description: Returns a binary value from the cluster database.
old-location: mscs\resutilgetbinaryvalue.htm
tech.root: MsCS
ms.assetid: d5068cc4-1fdc-430a-a48b-8e024bc20ca3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_BINARY_VALUE, PRESUTIL_GET_BINARY_VALUE function [Failover Cluster], ResUtilGetBinaryValue, ResUtilGetBinaryValue function [Failover Cluster], _wolf_resutilgetbinaryvalue, mscs.resutilgetbinaryvalue, resapi/PRESUTIL_GET_BINARY_VALUE, resapi/ResUtilGetBinaryValue
ms.topic: function
f1_keywords: ["resapi/ResUtilGetBinaryValue"]
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
 - ResUtilGetBinaryValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilGetBinaryValue function


## -description


Returns a binary value from the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

Key in the cluster database that identifies the location of the value to retrieve.


### -param pszValueName [in]

Pointer to a null-terminated Unicode string containing the name of the value to retrieve.


### -param ppbOutValue [out, optional]

Address of the pointer to the retrieved value.


### -param pcbOutValueSize [out]

Pointer to a <b>DWORD</b> in which the size in bytes of the buffer pointed to by <i>ppbOutValue</i> is returned.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

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
There was an error allocating memory for the value.

</td>
</tr>
</table>
 




## -remarks



The  <b>ResUtilGetBinaryValue</b> utility function takes care of allocating the necessary memory for the value and then calls the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-api">Cluster API</a> function  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>. When you are finished with the allocated memory, you must call the function  <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release it.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregqueryvalue">ClusterRegQueryValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetdwordvalue">ResUtilGetDwordValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nc-resapi-presutil_get_expand_sz_value">ResUtilGetExpandSzValue</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszvalue">ResUtilGetMultiSzValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetszvalue">ResUtilGetSzValue</a>
 

 

