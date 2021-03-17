---
UID: NF:ocidl.IClassFactory2.CreateInstanceLic
title: IClassFactory2::CreateInstanceLic (ocidl.h)
description: Creates an instance of the licensed object for the specified license key. This method is the only possible means to create an object on an otherwise unlicensed machine.
helpviewer_keywords: ["CreateInstanceLic","CreateInstanceLic method [COM]","CreateInstanceLic method [COM]","IClassFactory2 interface","IClassFactory2 interface [COM]","CreateInstanceLic method","IClassFactory2.CreateInstanceLic","IClassFactory2::CreateInstanceLic","_com_iclassfactory2_createinstancelic","com.iclassfactory2_createinstancelic","ocidl/IClassFactory2::CreateInstanceLic"]
old-location: com\iclassfactory2_createinstancelic.htm
tech.root: com
ms.assetid: f33c7223-da7d-4582-9a23-7dc34be97a9f
ms.date: 12/05/2018
ms.keywords: CreateInstanceLic, CreateInstanceLic method [COM], CreateInstanceLic method [COM],IClassFactory2 interface, IClassFactory2 interface [COM],CreateInstanceLic method, IClassFactory2.CreateInstanceLic, IClassFactory2::CreateInstanceLic, _com_iclassfactory2_createinstancelic, com.iclassfactory2_createinstancelic, ocidl/IClassFactory2::CreateInstanceLic
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
 - IClassFactory2::CreateInstanceLic
 - ocidl/IClassFactory2::CreateInstanceLic
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
 - IClassFactory2.CreateInstanceLic
---

# IClassFactory2::CreateInstanceLic


## -description

Creates an instance of the licensed object for the specified license key. This method is the only possible means to create an object on an otherwise unlicensed machine.

## -parameters

### -param pUnkOuter [in]

A pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the outer unknown if this object is being created as part of an aggregate. If the object is not part of an aggregate, this parameter must be <b>NULL</b>.

### -param pUnkReserved [in]

This parameter is unused and must be <b>NULL</b>.

### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the newly created object.

### -param bstrKey [in]

Run-time license key previously obtained from <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-requestlickey">IClassFactory2::RequestLicKey</a> that is required to create an object.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer. If an error occurs, the implementation must set *<i>ppvObj</i> to <b>NULL</b>.

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
The license was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented because objects can only be created on fully licensed machines through <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">IClassFactory::CreateInstance</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed in <i>bstrKey</i> or <i>ppvObj</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object can be created (and the license key is valid) except the object does not support the interface specified by <i>riid</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOAGGREGATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>pUnkOuter</i> parameter is non-<b>NULL</b>, but this object class does not support aggregation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOTLICENSED</b></dt>
</dl>
</td>
<td width="60%">
The key provided in <i>bstrKey</i> is not a valid license key.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the class factory does not provide a license key (that is, <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-requestlickey">IClassFactory2::RequestLicKey</a> returns E_NOTIMPL and the <b>fRuntimeKeyAvail</b> member in <a href="/windows/desktop/api/ocidl/ns-ocidl-licinfo">LICINFO</a> is set to <b>FALSE</b> in <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-getlicinfo">IClassFactory2::GetLicInfo</a>), then this method can also return E_NOTIMPL. In such cases, the class factory is implementing <a href="/windows/desktop/api/ocidl/nn-ocidl-iclassfactory2">IClassFactory2</a> simply to specify whether the machine is licensed at all through the <b>fLicVerified</b> member of <b>LICINFO</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iclassfactory2">IClassFactory2</a>



<a href="/windows/desktop/api/ocidl/ns-ocidl-licinfo">LICINFO</a>