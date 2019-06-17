---
UID: NF:rpcssl.RpcCertGeneratePrincipalNameW
title: RpcCertGeneratePrincipalNameW function (rpcssl.h)
author: windows-sdk-content
description: Server programs use the RpcCertGeneratePrincipalName function to generate principal names for security certificates.
old-location: rpc\rpccertgenerateprincipalname.htm
tech.root: Rpc
ms.assetid: 88a172f5-2226-46e9-845e-c67b0a885905
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RpcCertGeneratePrincipalName, RpcCertGeneratePrincipalName function [RPC], RpcCertGeneratePrincipalNameA, RpcCertGeneratePrincipalNameW, _rpc_rpccertgenerateprincipalname, rpc.rpccertgenerateprincipalname, rpcssl/RpcCertGeneratePrincipalName, rpcssl/RpcCertGeneratePrincipalNameA, rpcssl/RpcCertGeneratePrincipalNameW
ms.topic: function
f1_keywords: ["rpcssl/RpcCertGeneratePrincipalName"]
req.header: rpcssl.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcCertGeneratePrincipalNameW (Unicode) and RpcCertGeneratePrincipalNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcCertGeneratePrincipalName
 - RpcCertGeneratePrincipalNameA
 - RpcCertGeneratePrincipalNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcCertGeneratePrincipalNameW function


## -description


Server programs use the 
<b>RpcCertGeneratePrincipalName</b> function to generate 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/principal-names">principal names</a> for security certificates.


## -parameters




### -param Context

Pointer to the security-certificate context.


### -param Flags

Currently, the only valid flag for this parameter is RPC_C_FULL_CERT_CHAIN. Using this flag causes the principal name to be generated in fullsic format.


### -param pBuffer

Pointer to a pointer. The 
<b>RpcCertGeneratePrincipalName</b> function sets this to point at a null-terminated string that contains the 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/principal-names">principal name</a>.


## -returns



This function does not return a value.




## -remarks



By default, the principal name that the 
<b>RpcCertGeneratePrincipalName</b> function passes back is in msstd format. To generate a name in fullsic format, pass RPC_C_FULL_CERT_CHAIN as the value for the <i>Flags</i> parameter.

Your application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> to release the memory for the string which contains the principal name.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Rpc/principal-names">Principal Names</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
 

 

