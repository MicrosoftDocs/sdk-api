---
UID: NF:clusapi.ClusterResourceTypeControlAsUser
title: ClusterResourceTypeControlAsUser function
author: windows-sdk-content
description: Initiates an operation affecting a resource type.
old-location: mscs\clusterresourcetypecontrolasuser.htm
tech.root: MsCS
ms.assetid: 9F39952F-4B91-4C06-A789-D92F1F8462A4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterResourceTypeControlAsUser, ClusterResourceTypeControlAsUser function [Failover Cluster], clusapi/ClusterResourceTypeControlAsUser, mscs.clusterresourcetypecontrolasuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
api_name:
 - ClusterResourceTypeControlAsUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterResourceTypeControlAsUser
: 
---

# ClusterResourceTypeControlAsUser function


## -description


Initiates an operation affecting a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a>.

The 
    operation performed depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hCluster [in]

Handle to the cluster containing the resource type identified in 
       <i>lpszResourceTypeName</i>.


### -param lpszResourceTypeName [in]

Pointer to a <b>NULL</b>-terminated Unicode string containing the name of the resource 
       type to be affected.


### -param hHostNode [in, optional]

Handle to the node hosting the affected resource type.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa372232(v=VS.85).aspx">resource control code</a>, enumerated by the 
       <a href="https://msdn.microsoft.com/en-us/library/Cc307932(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_CODES</a> enumeration, 
       specifying the operation to be performed. For the syntax associated with a control code, refer to  the link on 
       the <b>CLUSCTL_RESOURCE_TYPE_CODES</b> topic.


### -param lpInBuffer [in, optional]

Pointer to the input buffer with information needed for the operation, or <b>NULL</b> if 
       no information is needed.


### -param nInBufferSize [in]

Number of bytes in the buffer pointed to by <i>lpInBuffer</i>.


### -param lpOutBuffer [out, optional]

Pointer to the output buffer with information resulting from the operation, or 
      <b>NULL</b> if nothing will be returned.


### -param nOutBufferSize [in]

Number of bytes in the output buffer pointed to by <i>lpOutBuffer</i>, or zero if the 
       caller does not know how much data will be returned.


### -param lpBytesReturned [out, optional]

Pointer to the number of bytes in the buffer pointed to by <i>lpOutBuffer</i> that were 
       actually filled in as a result of the operation. The caller can pass <b>NULL</b> for 
       <i>lpBytesReturned</i> if 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a> does not need 
       to pass back the number of bytes in the output buffer.


## -returns



The function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful. If the operation required an output buffer, 
         <i>lpBytesReturned</i> (if not <b>NULL</b> on input) points to the 
         actual size of the data returned in the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The output buffer pointed to by <i>lpOutBuffer</i> was not large enough to hold the data 
         resulting from the operation. The <i>lpBytesReturned</i> parameter (if not 
         <b>NULL</b> on input) points to the size required for the output buffer. Only operations 
         requiring an output buffer return <b>ERROR_MORE_DATA</b>. If the 
         <i>lpOutBuffer</i> parameter is <b>NULL</b> and the 
         <i>nOutBufferSize</i> parameter is zero, then <b>ERROR_SUCCESS</b> may 
         be returned, not <b>ERROR_MORE_DATA</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. If the operation required an output buffer, the value specified by 
         <i>lpBytesReturned</i> is unreliable.

</td>
</tr>
</table>
 




## -remarks



When <a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.


<a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372309(v=VS.85).aspx">Resource Type Control Codes</a>
 

 

