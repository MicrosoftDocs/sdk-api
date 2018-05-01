---
UID: NF:ntdsapi.DsClientMakeSpnForTargetServerW
title: DsClientMakeSpnForTargetServerW function
author: windows-driver-content
description: Constructs a service principal name (SPN) that identifies a specific server to use for authentication.
old-location: ad\dsclientmakespnfortargetserver.htm
old-project: AD
ms.assetid: d205e7cc-4879-41a4-baa7-75e7dd177cd0
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: DsClientMakeSpnForTargetServer, DsClientMakeSpnForTargetServer function [Active Directory], DsClientMakeSpnForTargetServerA, DsClientMakeSpnForTargetServerW, _glines_dsclientmakespnfortargetserver, ad.dsclientmakespnfortargetserver, ntdsapi/DsClientMakeSpnForTargetServer, ntdsapi/DsClientMakeSpnForTargetServerA, ntdsapi/DsClientMakeSpnForTargetServerW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsClientMakeSpnForTargetServerW (Unicode) and DsClientMakeSpnForTargetServerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsClientMakeSpnForTargetServer
-	DsClientMakeSpnForTargetServerA
-	DsClientMakeSpnForTargetServerW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DsClientMakeSpnForTargetServerW function


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
 

 

