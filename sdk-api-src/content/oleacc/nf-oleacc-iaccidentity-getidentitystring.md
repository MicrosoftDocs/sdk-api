---
UID: NF:oleacc.IAccIdentity.GetIdentityString
title: IAccIdentity::GetIdentityString (oleacc.h)
description: Retrieves a string of bytes (an identity string) that uniquely identifies an accessible element.
helpviewer_keywords: ["GetIdentityString","GetIdentityString method [Windows Accessibility]","GetIdentityString method [Windows Accessibility]","IAccIdentity interface","IAccIdentity interface [Windows Accessibility]","GetIdentityString method","IAccIdentity.GetIdentityString","IAccIdentity::GetIdentityString","_msaa_IAccIdentity_GetIdentityString","msaa.iaccidentity_iaccidentity__getidentitystring","oleacc/IAccIdentity::GetIdentityString","winauto.iaccidentity_iaccidentity__getidentitystring"]
old-location: winauto\iaccidentity_iaccidentity__getidentitystring.htm
tech.root: WinAuto
ms.assetid: 38467491-c432-456a-9128-723fc7dde189
ms.date: 12/05/2018
ms.keywords: GetIdentityString, GetIdentityString method [Windows Accessibility], GetIdentityString method [Windows Accessibility],IAccIdentity interface, IAccIdentity interface [Windows Accessibility],GetIdentityString method, IAccIdentity.GetIdentityString, IAccIdentity::GetIdentityString, _msaa_IAccIdentity_GetIdentityString, msaa.iaccidentity_iaccidentity__getidentitystring, oleacc/IAccIdentity::GetIdentityString, winauto.iaccidentity_iaccidentity__getidentitystring
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows Vista or Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccIdentity::GetIdentityString
 - oleacc/IAccIdentity::GetIdentityString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccIdentity.GetIdentityString
---

# IAccIdentity::GetIdentityString


## -description

Retrieves a string of bytes (an identity string) that uniquely identifies an accessible element.

If server developers know the <b>HWND</b> of the object they want to annotate, they can use one of the following methods instead of using this 
		method and getting an identity string.
<ul>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">IAccPropServices::SetHwndPropStr</a>
</li>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">IAccPropServices::SetHwndProp</a>
</li>
<li>
<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">IAccPropServices::SetHwndPropServer</a>
</li>
</ul>

## -parameters

### -param dwIDChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies which child of the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object the caller wants to identify.

### -param ppIDString [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>**</b>

Address of a variable that receives a pointer to a callee-allocated identity string. The callee allocates the identity string using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>; the caller must release the identity string by using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when finished.

### -param pdwIDStringLen [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Address of a variable that receives the length, in bytes, of the callee-allocated identity string.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK, except under exceptional error conditions, such as low memory. If not supported, calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccidentity">IAccIdentity</a> should fail.

## -remarks

The returned string should be considered opaque; clients should use it only as a whole, and should not attempt to dissect it or otherwise interpret it manually.

If a client knows or expects that a string is HWND—based, it can use <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-decomposehwndidentitystring">IAccPropServices::DecomposeHwndIdentityString</a> to attempt to decompose the identity string.