---
UID: NF:ocidl.IClassFactory2.CreateInstanceLic
title: IClassFactory2::CreateInstanceLic
author: windows-driver-content
description: Creates an instance of the licensed object for the specified license key. This method is the only possible means to create an object on an otherwise unlicensed machine.
old-location: com\iclassfactory2_createinstancelic.htm
old-project: com
ms.assetid: f33c7223-da7d-4582-9a23-7dc34be97a9f
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CreateInstanceLic, CreateInstanceLic method [COM], CreateInstanceLic method [COM],IClassFactory2 interface, IClassFactory2 interface [COM],CreateInstanceLic method, IClassFactory2.CreateInstanceLic, IClassFactory2::CreateInstanceLic, _com_iclassfactory2_createinstancelic, com.iclassfactory2_createinstancelic, ocidl/IClassFactory2::CreateInstanceLic
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IClassFactory2.CreateInstanceLic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IClassFactory2::CreateInstanceLic


## -description


Creates an instance of the licensed object for the specified license key. This method is the only possible means to create an object on an otherwise unlicensed machine.


## -parameters




### -param pUnkOuter [in]

A pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the outer unknown if this object is being created as part of an aggregate. If the object is not part of an aggregate, this parameter must be <b>NULL</b>.


### -param pUnkReserved [in]

This parameter is unused and must be <b>NULL</b>.


### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the newly created object.


### -param bstrKey [in]

Run-time license key previously obtained from <a href="https://msdn.microsoft.com/6c0211d2-1cdd-4d1a-a1fe-44c89b750af6">IClassFactory2::RequestLicKey</a> that is required to create an object.


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
This method is not implemented because objects can only be created on fully licensed machines through <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a>.

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
If the class factory does not provide a license key (that is, <a href="https://msdn.microsoft.com/6c0211d2-1cdd-4d1a-a1fe-44c89b750af6">IClassFactory2::RequestLicKey</a> returns E_NOTIMPL and the <b>fRuntimeKeyAvail</b> member in <a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a> is set to <b>FALSE</b> in <a href="https://msdn.microsoft.com/e55d1089-b1df-4de0-9a19-cbd255b36126">IClassFactory2::GetLicInfo</a>), then this method can also return E_NOTIMPL. In such cases, the class factory is implementing <a href="https://msdn.microsoft.com/c49c7612-3b1f-4535-baf3-8458b3f34f95">IClassFactory2</a> simply to specify whether the machine is licensed at all through the <b>fLicVerified</b> member of <b>LICINFO</b>.




## -see-also




<a href="https://msdn.microsoft.com/c49c7612-3b1f-4535-baf3-8458b3f34f95">IClassFactory2</a>



<a href="https://msdn.microsoft.com/a90d82f3-8dc4-4b1d-81f7-9d3a19e74314">LICINFO</a>
 

 

