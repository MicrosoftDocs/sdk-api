---
UID: NF:ocidl.IObjectWithSite.GetSite
title: IObjectWithSite::GetSite (ocidl.h)
description: Retrieves the latest site passed using SetSite.
helpviewer_keywords: ["GetSite","GetSite method [COM]","GetSite method [COM]","IObjectWithSite interface","IObjectWithSite interface [COM]","GetSite method","IObjectWithSite.GetSite","IObjectWithSite::GetSite","_ole_iobjectwithsite_getsite","com.iobjectwithsite_getsite","ocidl/IObjectWithSite::GetSite"]
old-location: com\iobjectwithsite_getsite.htm
tech.root: com
ms.assetid: f88ef2b1-63c3-4307-a5e1-b9104c8aef29
ms.date: 12/05/2018
ms.keywords: GetSite, GetSite method [COM], GetSite method [COM],IObjectWithSite interface, IObjectWithSite interface [COM],GetSite method, IObjectWithSite.GetSite, IObjectWithSite::GetSite, _ole_iobjectwithsite_getsite, com.iobjectwithsite_getsite, ocidl/IObjectWithSite::GetSite
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IObjectWithSite::GetSite
 - ocidl/IObjectWithSite::GetSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IObjectWithSite.GetSite
---

# IObjectWithSite::GetSite


## -description

Retrieves the latest site passed using <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a>.

## -parameters

### -param riid [in]

The IID of the interface pointer that should be returned in <i>ppvSite</i>.

### -param ppvSite [out]

Address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvSite</i> contains the requested interface pointer to the site last seen in <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a>. The specific interface returned depends on the <i>riid</i> argument. In essence, the two arguments act identically to those in <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. If the appropriate interface pointer is available, the object must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on that pointer before returning successfully. If no site is available, or the requested interface is not supported, this method must *<i>ppvSite</i> to <b>NULL</b> and return a failure code.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no site, in which case *<i>ppvSite</i> contains <b>NULL</b> on return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
There is a site, but it does not support the interface requested by <i>riid</i>.

</td>
</tr>
</table>

## -remarks

E_NOTIMPL is not allowed. Any object implementing this interface must be able to return the last site seen in <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a>