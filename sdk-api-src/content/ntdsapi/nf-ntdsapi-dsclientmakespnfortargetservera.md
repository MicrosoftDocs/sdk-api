---
UID: NF:ntdsapi.DsClientMakeSpnForTargetServerA
title: DsClientMakeSpnForTargetServerA function (ntdsapi.h)
author: windows-sdk-content
description: Constructs a service principal name (SPN) that identifies a specific server to use for authentication.
old-location: ad\dsclientmakespnfortargetserver.htm
tech.root: ad
ms.assetid: d205e7cc-4879-41a4-baa7-75e7dd177cd0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsClientMakeSpnForTargetServer, DsClientMakeSpnForTargetServer function [Active Directory], DsClientMakeSpnForTargetServerA, DsClientMakeSpnForTargetServerW, _glines_dsclientmakespnfortargetserver, ad.dsclientmakespnfortargetserver, ntdsapi/DsClientMakeSpnForTargetServer, ntdsapi/DsClientMakeSpnForTargetServerA, ntdsapi/DsClientMakeSpnForTargetServerW
ms.topic: function
f1_keywords: 
 - "ntdsapi/DsClientMakeSpnForTargetServer"
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
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsClientMakeSpnForTargetServer
 - DsClientMakeSpnForTargetServerA
 - DsClientMakeSpnForTargetServerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

This function is a simplified version of the <a href="https://docs.microsoft.com/windows/desktop/api/dsparse/nf-dsparse-dsmakespna">DsMakeSpn</a> function. The <i>ServiceName</i> is made canonical by resolving through DNS.

GUID-based DNS names are not supported. When constructed, the simplified SPN is as follows:

<pre class="syntax" xml:space="preserve"><code>ServiceClass / ServiceName / ServiceName</code></pre>
The instance name portion (second position) is always set to default. The port and referrer fields are not used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsparse/nf-dsparse-dsmakespna">DsMakeSpn</a>
 

 

