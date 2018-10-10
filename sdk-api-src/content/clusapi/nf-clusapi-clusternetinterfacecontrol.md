---
UID: NF:clusapi.ClusterNetInterfaceControl
title: ClusterNetInterfaceControl function
author: windows-sdk-content
description: Initiates an operation that affects a network interface. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternetinterfacecontrol.htm
tech.root: MsCS
ms.assetid: cfb56e61-3652-47a3-860b-706e6dba03d7
ms.author: windowssdkdev
ms.date: 10/05/2018
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
---

# ClusterNetInterfaceControl function


## -description


Initiates an operation that affects a <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>. 
    The operation performed depends on the <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to 
    the <i>dwControlCode</i> parameter.


## -parameters




### -param hNetInterface [in]

Handle to the network interface to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> that 
       owns the network interface to be affected. If <b>NULL</b>, the local node performs the 
       operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/adc97081-e778-426d-8296-9dea9f22a4e4">network interface control code</a> 
       specifying the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/cedac89a-121d-4d74-ac06-4723d292f3e7">CLUSCTL_NETINTERFACE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/464aadac-8d95-478c-b9ee-9101cad6d99a">CLUSCTL_NETINTERFACE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5ead5c71-0a35-44c3-aa77-c7c4b8bb197b">CLUSCTL_NETINTERFACE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d83b0eb5-3043-4466-8ed5-2dde96073d49">CLUSCTL_NETINTERFACE_GET_COMMON_PROPERTIES</a>
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
<a href="https://msdn.microsoft.com/580a515c-271c-4774-adf7-a41eae5023f3">CLUSCTL_NETINTERFACE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f3cd817d-688c-4062-a407-c5119bbe7db5">CLUSCTL_NETINTERFACE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/015acd68-8648-49fa-9484-5afb6b361492">CLUSCTL_NETINTERFACE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/679ec15c-e66f-498a-8bf9-0c391b41199d">CLUSCTL_NETINTERFACE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f022e475-d6b8-4ac7-86ac-ef5692667421">CLUSCTL_NETINTERFACE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0698ee19-d560-4e4c-a7ce-6fcf4ff061ae">CLUSCTL_NETINTERFACE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12061a66-bc72-4ce2-ba6c-90a8e321d8f3">CLUSCTL_NETINTERFACE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06836f31-a9df-4624-b9c1-31a88d974e19">CLUSCTL_NETINTERFACE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5bc41c4a-ec42-4f29-bd49-18daf3a18275">CLUSCTL_NETINTERFACE_VALIDATE_PRIVATE_PROPERTIES</a>
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




## -remarks



If <b>ClusterNetInterfaceControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNetInterfaceControl</b> is one of 
     the <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/adc97081-e778-426d-8296-9dea9f22a4e4">Network Interface Control Codes</a>
 

 

