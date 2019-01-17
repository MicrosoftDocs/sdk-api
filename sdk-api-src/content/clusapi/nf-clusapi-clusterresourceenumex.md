---
UID: NF:clusapi.ClusterResourceEnumEx
title: ClusterResourceEnumEx function
author: windows-sdk-content
description: Enumerates a resource and then returns a pointer to the current dependent resource or node.
old-location: mscs\clusterresourceenumex.htm
tech.root: MsCS
ms.assetid: 9B5C03DF-84BB-4B3A-8404-94C64F192305
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterResourceEnumEx, ClusterResourceEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX function [Failover Cluster], clusapi/ClusterResourceEnumEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_ENUM_EX, mscs.clusterresourceenumex
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterResourceEnumEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceEnumEx function


## -description


Enumerates a resource and then returns a pointer to the current  dependent resource or node.


## -parameters




### -param hResourceEnumEx [in]

A handle to a resource enumeration   that is returned from 
       the <a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a> function.


### -param dwIndex [in]

The index of the resource or node object to return. This parameter should be zero for the first call to the 
       <b>ClusterResourceEnumEx</b> function and then be  
       incremented for subsequent calls.


### -param pItem [in, out]

A pointer that receives the returned object.


### -param cbItem [in, out]

On input, the size of the  <i>pItem</i> parameter.

On output, either the required size in bytes of the buffer if the buffer is too small, or the number of bytes written into the buffer.


## -returns



The function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation finished  successfully, or the <i>lpszName</i> parameter is 
         <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The buffer to which   the <i>lpszName</i> parameter points is not big enough to hold the 
         result. The <i>lpcchName</i> parameter returns the number of characters in the result, 
         excluding the terminating null character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
There are no more objects to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
Any other returned error code indicates that the operation failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B43460F1-4BFE-48E0-889A-56370320E4E6">ClusterResourceOpenEnumEx</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

