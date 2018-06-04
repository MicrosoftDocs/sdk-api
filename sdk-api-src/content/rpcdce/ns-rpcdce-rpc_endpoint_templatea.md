---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RPC_ENDPOINT_TEMPLATEA structure


## -description


The <b>RPC_ENDPOINT_TEMPLATE</b> structure specifies the properties of an RPC interface group server endpoint, including protocol sequence and name.


## -struct-fields




### -field Version

This field is reserved and must be set to 0.


### -field ProtSeq

Pointer to a string identifier of the protocol sequence to register with the RPC run-time library.  Only <a href="https://msdn.microsoft.com/51284532-b0ac-4bf2-b322-91393b2b9dc6">ncalrpc</a>, ncacn_ip_tcp, and ncacn_np are supported.  This value must not be <b>NULL</b>.


### -field Endpoint

Optional pointer to the endpoint-address information to use in creating a binding for the protocol sequence specified in the <i>Protseq</i> parameter.  Specify <b>NULL</b> to use dynamic endpoints.


### -field SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <a href="https://msdn.microsoft.com/51284532-b0ac-4bf2-b322-91393b2b9dc6">ncacn_np</a> and ncalrpc protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended.


### -field Backlog

Backlog queue length for the <a href="https://msdn.microsoft.com/51284532-b0ac-4bf2-b322-91393b2b9dc6">ncacn_ip_tcp</a> protocol sequence. All other protocol sequences ignore this parameter. Use <b>RPC_C_PROTSEQ_MAX_REQS_DEFAULT</b> to specify the default value.  See Remarks for more informatation.


## -remarks



The value provided in <i>Backlog</i> by applications is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>Backlog</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted.

An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>Backlog</i>.




## -see-also




<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInqBindings</a>
 

 

