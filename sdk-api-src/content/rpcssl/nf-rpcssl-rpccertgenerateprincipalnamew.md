---
UID: NF:rpcssl.RpcCertGeneratePrincipalNameW
title: RpcCertGeneratePrincipalNameW function (rpcssl.h)
description: The RpcCertGeneratePrincipalNameW (Unicode) function (rpcssl.h) is used by server programs to generate principal names for security certificates.
helpviewer_keywords: ["RpcCertGeneratePrincipalName", "RpcCertGeneratePrincipalName function [RPC]", "RpcCertGeneratePrincipalNameW", "_rpc_rpccertgenerateprincipalname", "rpc.rpccertgenerateprincipalname", "rpcssl/RpcCertGeneratePrincipalName", "rpcssl/RpcCertGeneratePrincipalNameW"]
old-location: rpc\rpccertgenerateprincipalname.htm
tech.root: Rpc
ms.assetid: 88a172f5-2226-46e9-845e-c67b0a885905
ms.date: 08/15/2022
ms.keywords: RpcCertGeneratePrincipalName, RpcCertGeneratePrincipalName function [RPC], RpcCertGeneratePrincipalNameA, RpcCertGeneratePrincipalNameW, _rpc_rpccertgenerateprincipalname, rpc.rpccertgenerateprincipalname, rpcssl/RpcCertGeneratePrincipalName, rpcssl/RpcCertGeneratePrincipalNameA, rpcssl/RpcCertGeneratePrincipalNameW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcCertGeneratePrincipalNameW
 - rpcssl/RpcCertGeneratePrincipalNameW
dev_langs:
 - c++
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
---

# RpcCertGeneratePrincipalNameW function


## -description

Server programs use the 
<b>RpcCertGeneratePrincipalName</b> function to generate 
<a href="/windows/desktop/Rpc/principal-names">principal names</a> for security certificates.

## -parameters

### -param Context

Pointer to the security-certificate context.

### -param Flags

Currently, the only valid flag for this parameter is RPC_C_FULL_CERT_CHAIN. Using this flag causes the principal name to be generated in fullsic format.

### -param pBuffer

Pointer to a pointer. The 
<b>RpcCertGeneratePrincipalName</b> function sets this to point at a null-terminated string that contains the 
<a href="/windows/desktop/Rpc/principal-names">principal name</a>.

## -returns

This function does not return a value.

## -remarks

By default, the principal name that the 
<b>RpcCertGeneratePrincipalName</b> function passes back is in msstd format. To generate a name in fullsic format, pass RPC_C_FULL_CERT_CHAIN as the value for the <i>Flags</i> parameter.

Your application must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> to release the memory for the string which contains the principal name.





> [!NOTE]
> The rpcssl.h header defines RpcCertGeneratePrincipalName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Rpc/principal-names">Principal Names</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
