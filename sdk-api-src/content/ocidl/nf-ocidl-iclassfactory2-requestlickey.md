---
UID: NF:ocidl.IClassFactory2.RequestLicKey
title: IClassFactory2::RequestLicKey (ocidl.h)
description: Creates a license key that the caller can save and use later to create an instance of the licensed object.
helpviewer_keywords: ["IClassFactory2 interface [COM]","RequestLicKey method","IClassFactory2.RequestLicKey","IClassFactory2::RequestLicKey","RequestLicKey","RequestLicKey method [COM]","RequestLicKey method [COM]","IClassFactory2 interface","_com_iclassfactory2_requestlickey","com.iclassfactory2_requestlickey","ocidl/IClassFactory2::RequestLicKey"]
old-location: com\iclassfactory2_requestlickey.htm
tech.root: com
ms.assetid: 6c0211d2-1cdd-4d1a-a1fe-44c89b750af6
ms.date: 12/05/2018
ms.keywords: IClassFactory2 interface [COM],RequestLicKey method, IClassFactory2.RequestLicKey, IClassFactory2::RequestLicKey, RequestLicKey, RequestLicKey method [COM], RequestLicKey method [COM],IClassFactory2 interface, _com_iclassfactory2_requestlickey, com.iclassfactory2_requestlickey, ocidl/IClassFactory2::RequestLicKey
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
 - IClassFactory2::RequestLicKey
 - ocidl/IClassFactory2::RequestLicKey
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
 - IClassFactory2.RequestLicKey
---

# IClassFactory2::RequestLicKey


## -description

Creates a license key that the caller can save and use later to create an instance of the licensed object.

## -parameters

### -param dwReserved [in]

This parameter is reserved and must be zero.

### -param pBstrKey [out]

A pointer to the caller-allocated variable that receives the callee-allocated license key on successful return from this method. This parameter is set to <b>NULL</b> on any failure.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The license key was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This class factory does not support run-time license keys.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address passed in <i>pbstrKey</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOTLICENSED</b></dt>
</dl>
</td>
<td width="60%">
This class factory supports run-time licensing, but the current machine itself is not licensed. Thus, a run-time key is not available on this machine.

</td>
</tr>
</table>

## -remarks

The caller can save the license key for subsequent calls to <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-createinstancelic">IClassFactory2::CreateInstanceLic</a> to create objects on an otherwise unlicensed machine.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller must free the <b>BSTR</b> with the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function when the key is no longer needed. The value of <i>fRuntimeKeyAvail</i> is returned through a previous call to <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-getlicinfo">IClassFactory2::GetLicInfo</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method allocates the <b>BSTR</b> key with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> or <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringlen">SysAllocStringLen</a>, and the caller becomes responsible for this <b>BSTR</b> after this method returns successfully.

This method need not be implemented when a class factory does not support run-time license keys.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iclassfactory2">IClassFactory2</a>