---
UID: NF:clusapi.ClusterNetInterfaceControl
title: ClusterNetInterfaceControl function
author: windows-sdk-content
description: Initiates an operation that affects a network interface. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternetinterfacecontrol.htm
tech.root: MsCS
ms.assetid: cfb56e61-3652-47a3-860b-706e6dba03d7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterNetInterfaceControl, ClusterNetInterfaceControl function [Failover Cluster], _wolf_clusternetinterfacecontrol, clusapi/ClusterNetInterfaceControl, mscs.clusternetinterfacecontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
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
 - ClusterNetInterfaceControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterNetInterfaceControl
: 
---

# ClusterNetInterfaceControl function


## -description


Initiates an operation that affects a <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>. 
    The operation performed depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to 
    the <i>dwControlCode</i> parameter.


## -parameters




### -param hNetInterface [in]

Handle to the network interface to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> that 
       owns the network interface to be affected. If <b>NULL</b>, the local node performs the 
       operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa371723(v=VS.85).aspx">network interface control code</a> 
       specifying the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367256(v=VS.85).aspx">CLUSCTL_NETINTERFACE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367257(v=VS.85).aspx">CLUSCTL_NETINTERFACE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367258(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367259(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bfd17e43-0288-4f5d-835c-41a7e023c79e">CLUSCTL_NETINTERFACE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e356749-18ee-4e64-84cc-8fd5f5775869">CLUSCTL_NETINTERFACE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d83c1146-a063-44c0-a236-b82ae90f5e2e">CLUSCTL_NETINTERFACE_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aace3b0c-0e7f-451e-ac58-721438bd4b0e">CLUSCTL_NETINTERFACE_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/13dd855d-1e52-466c-8709-5d6a5fd8e73c">CLUSCTL_NETINTERFACE_GET_NETWORK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f5d049e-73b6-4e2c-a5d4-36bbb03638a9">CLUSCTL_NETINTERFACE_GET_NODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367266(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367267(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367268(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367269(v=VS.85).aspx">CLUSCTL_NETINTERFACE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367392(v=VS.85).aspx">CLUSCTL_NETINTERFACE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367393(v=VS.85).aspx">CLUSCTL_NETINTERFACE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367394(v=VS.85).aspx">CLUSCTL_NETINTERFACE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367395(v=VS.85).aspx">CLUSCTL_NETINTERFACE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367396(v=VS.85).aspx">CLUSCTL_NETINTERFACE_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>



### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param nInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param nOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


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
         <i>lpBytesReturned</i> (if not <b>NULL</b> on input) points to the actual size of the data 
         returned in the buffer.

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
         <i>lpBytesReturned</i> (if not <b>NULL</b> on input) is unreliable.

</td>
</tr>
</table>
 




## -remarks



If <b>ClusterNetInterfaceControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNetInterfaceControl</b> is one of 
     the <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa371723(v=VS.85).aspx">Network Interface Control Codes</a>
 

 

