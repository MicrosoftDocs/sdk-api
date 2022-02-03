---
UID: NF:combaseapi.CoCopyProxy
title: CoCopyProxy function (combaseapi.h)
description: Makes a private copy of the specified proxy.
helpviewer_keywords: ["CoCopyProxy","CoCopyProxy function [COM]","_com_CoCopyProxy","com.cocopyproxy","combaseapi/CoCopyProxy"]
old-location: com\cocopyproxy.htm
tech.root: com
ms.assetid: 26de7bac-8745-40c0-be0a-dcec88a3ecaf
ms.date: 12/05/2018
ms.keywords: CoCopyProxy, CoCopyProxy function [COM], _com_CoCopyProxy, com.cocopyproxy, combaseapi/CoCopyProxy
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoCopyProxy
 - combaseapi/CoCopyProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoCopyProxy
---

# CoCopyProxy function


## -description

Makes a private copy of the specified proxy.

## -parameters

### -param pProxy [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the proxy to be copied. This parameter cannot be <b>NULL</b>.

### -param ppCopy [out]

Address of the pointer variable that receives the interface pointer to the copy of the proxy. This parameter cannot be <b>NULL</b>.

## -returns

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>

## -remarks

<b>CoCopyProxy</b> makes a private copy of the specified proxy. Typically, this function is called when a client needs to change the authentication information of its proxy through a call to either <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a> or <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> without changing this information for other clients. <b>CoSetProxyBlanket</b> affects all the users of an instance of a proxy, so creating a private copy of the proxy through a call to <b>CoCopyProxy</b> and then calling <b>CoSetProxyBlanket</b> (or <b>IClientSecurity::SetBlanket</b>) using the copy eliminates the problem.

This helper function encapsulates the following sequence of common calls (error handling excluded):




``` syntax
    pProxy->QueryInterface(IID_IClientSecurity, (void**)&pcs);
    pcs->CopyProxy(punkProxy, ppunkCopy);
    pcs->Release();
```

Local interfaces may not be copied. <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> are examples of existing local interfaces.

Copies of the same proxy have a special relationship with respect to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. Given a proxy, a, of the IA interface of a remote object, suppose a copy of a is created, called b. In this case, calling <b>QueryInterface</b> from the b proxy for IID_IA will not retrieve the IA interface on b, but the one on a, the original proxy with the "default" security settings for the IA interface.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>
