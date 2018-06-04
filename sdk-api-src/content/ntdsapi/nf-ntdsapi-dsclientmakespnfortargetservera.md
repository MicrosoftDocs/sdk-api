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

# DsClientMakeSpnForTargetServerA function


## -description


The <b>DsClientMakeSpnForTargetServer</b> function constructs a service principal name (SPN) that identifies a specific server to use for authentication.


## -parameters




### -param ServiceClass [in]

Pointer to a null-terminated string that contains the class of the service as defined by the service. This can be any string unique to the service.


### -param ServiceName [in]

Pointer to a null-terminated string that contains the distinguished name service (DNS) host name. This can either be a fully qualified name or an IP address in the Internet standard  format.

Use of an IP address for <i>ServiceName</i> is not recommended because this can create a security issue. Before the SPN is constructed, the IP address must be translated to a computer name through DNS name resolution. It is possible for the DNS name resolution to be spoofed, replacing the  intended computer name with an unauthorized computer name.


### -param pcSpnLength [in, out]

Pointer to a <b>DWORD</b> value that, on entry, contains the size of the <i>pszSpn</i> buffer, in characters. On output, this parameter receives the number of characters copied to the  <i>pszSpn</i> buffer, including the terminating <b>NULL</b>.


### -param pszSpn [out]

Pointer to a string buffer that receives the SPN.


## -returns



This function returns standard Windows error codes.




## -remarks



When using this function, supply the service class and part of a DNS host name.

This function is a simplified version of the <a href="https://msdn.microsoft.com/fca3c59c-bb81-42a0-acd3-2e55c902febe">DsMakeSpn</a> function. The <i>ServiceName</i> is made canonical by resolving through DNS.

GUID-based DNS names are not supported. When constructed, the simplified SPN is as follows:

<pre class="syntax" xml:space="preserve"><code>ServiceClass / ServiceName / ServiceName</code></pre>
The instance name portion (second position) is always set to default. The port and referrer fields are not used.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/fca3c59c-bb81-42a0-acd3-2e55c902febe">DsMakeSpn</a>
 

 

