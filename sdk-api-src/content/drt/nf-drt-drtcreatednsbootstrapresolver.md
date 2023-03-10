---
UID: NF:drt.DrtCreateDnsBootstrapResolver
title: DrtCreateDnsBootstrapResolver function (drt.h)
description: The DrtCreateDnsBootstrapResolver function creates a bootstrap resolver that will use the GetAddrInfo system function to resolve the hostname of a will known node already present in the DRT mesh.
helpviewer_keywords: ["DrtCreateDnsBootstrapResolver","DrtCreateDnsBootstrapResolver function [Distributed Routing Tables]","drt/DrtCreateDnsBootstrapResolver","p2p.drtcreatednsbootstrapresolver"]
old-location: p2p\drtcreatednsbootstrapresolver.htm
tech.root: p2p
ms.assetid: d4a92dd3-d66a-4c27-9180-f9c148735a4a
ms.date: 12/05/2018
ms.keywords: DrtCreateDnsBootstrapResolver, DrtCreateDnsBootstrapResolver function [Distributed Routing Tables], drt/DrtCreateDnsBootstrapResolver, p2p.drtcreatednsbootstrapresolver
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtCreateDnsBootstrapResolver
 - drt/DrtCreateDnsBootstrapResolver
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateDnsBootstrapResolver
---

# DrtCreateDnsBootstrapResolver function


## -description

The <b>DrtCreateDnsBootstrapResolver</b> function creates a bootstrap resolver that will use the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfo</a> system function to resolve the hostname of a will known node already present in the DRT mesh.

## -parameters

### -param port [in]

Specifies the port to which the DRT protocol is bound on the well known node.

### -param pwszAddress [in]

Specifies the hostname of the well known node.

### -param ppModule [out]

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider">DRT_BOOTSTRAP_PROVIDER</a> module to be included in the <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> structure.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszAddress</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system could not allocate memory for the provider.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also return errors from underlying calls to <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> and StringCbPrintfW.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider">DRT_BOOTSTRAP_PROVIDER</a>



<a href="/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver">DrtDeleteDnsBootstrapResolver</a>