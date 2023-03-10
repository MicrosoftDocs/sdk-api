---
UID: NF:objidl.IClientSecurity.CopyProxy
title: IClientSecurity::CopyProxy (objidl.h)
description: Makes a private copy of the proxy for the specified interface.
helpviewer_keywords: ["CopyProxy","CopyProxy method [COM]","CopyProxy method [COM]","IClientSecurity interface","IClientSecurity interface [COM]","CopyProxy method","IClientSecurity.CopyProxy","IClientSecurity::CopyProxy","_com_iclientsecurity_copyproxy","com.iclientsecurity_copyproxy","objidlbase/IClientSecurity::CopyProxy"]
old-location: com\iclientsecurity_copyproxy.htm
tech.root: com
ms.assetid: 4664351b-d43b-45dc-800e-574685afd0f6
ms.date: 12/05/2018
ms.keywords: CopyProxy, CopyProxy method [COM], CopyProxy method [COM],IClientSecurity interface, IClientSecurity interface [COM],CopyProxy method, IClientSecurity.CopyProxy, IClientSecurity::CopyProxy, _com_iclientsecurity_copyproxy, com.iclientsecurity_copyproxy, objidlbase/IClientSecurity::CopyProxy
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClientSecurity::CopyProxy
 - objidl/IClientSecurity::CopyProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IClientSecurity.CopyProxy
---

# IClientSecurity::CopyProxy


## -description

Makes a private copy of the proxy for the specified interface.

## -parameters

### -param pProxy [in]

A pointer to the interface whose proxy is to be copied. This parameter cannot be <b>NULL</b>.

### -param ppCopy [out]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer that receives the copy of the proxy. This parameter cannot be <b>NULL</b>.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>

## -remarks

<b>CopyProxy</b> is called by the client to make a private copy of the proxy for the specified interface. The proxy copy has default values for the authentication information. Its authentication information can be changed through a call to <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> without affecting any other clients of the original proxy. The copy has one reference, and the caller of <b>CopyProxy</b> must ensure that the proxy copy gets freed.

Local interfaces, such as <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>, cannot be copied. You cannot duplicate a proxy manager using <b>CopyProxy</b>.

Copies of the same proxy have a special relationship with respect to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. Given a proxy, a, of the IA interface of a remote object, suppose a copy of a is created, called b. In this case, calling <b>QueryInterface</b> from the b proxy for IID_IA will not retrieve the IA interface on b, but the one on a, the original proxy.

Notice that anyone can query for a proxy and change security on it using <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">SetBlanket</a>. However, when you have made a copy of a proxy, no one can get the copy unless you give it to them. Only people who have the copy can set security on it.

The helper function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy">CoCopyProxy</a> encapsulates a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call for a pointer to IClientSecurity, a call to <b>CopyProxy</b> with the <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> pointer, and the release of the <b>IClientSecurity</b> pointer.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy">CoCopyProxy</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>