---
UID: NF:msctf.ITfPersistentPropertyLoaderACP.LoadProperty
title: ITfPersistentPropertyLoaderACP::LoadProperty (msctf.h)
description: ITfPersistentPropertyLoaderACP::LoadProperty method
helpviewer_keywords: ["ITfPersistentPropertyLoaderACP interface [Text Services Framework]","LoadProperty method","ITfPersistentPropertyLoaderACP.LoadProperty","ITfPersistentPropertyLoaderACP::LoadProperty","LoadProperty","LoadProperty method [Text Services Framework]","LoadProperty method [Text Services Framework]","ITfPersistentPropertyLoaderACP interface","_tsf_itfpersistentpropertyloaderacp_loadproperty_ref","msctf/ITfPersistentPropertyLoaderACP::LoadProperty","tsf.itfpersistentpropertyloaderacp_loadproperty"]
old-location: tsf\itfpersistentpropertyloaderacp_loadproperty.htm
tech.root: TSF
ms.assetid: 20730a90-e59c-46ae-a0bf-a212b201351c
ms.date: 12/05/2018
ms.keywords: ITfPersistentPropertyLoaderACP interface [Text Services Framework],LoadProperty method, ITfPersistentPropertyLoaderACP.LoadProperty, ITfPersistentPropertyLoaderACP::LoadProperty, LoadProperty, LoadProperty method [Text Services Framework], LoadProperty method [Text Services Framework],ITfPersistentPropertyLoaderACP interface, _tsf_itfpersistentpropertyloaderacp_loadproperty_ref, msctf/ITfPersistentPropertyLoaderACP::LoadProperty, tsf.itfpersistentpropertyloaderacp_loadproperty
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfPersistentPropertyLoaderACP::LoadProperty
 - msctf/ITfPersistentPropertyLoaderACP::LoadProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfPersistentPropertyLoaderACP.LoadProperty
---

# ITfPersistentPropertyLoaderACP::LoadProperty


## -description

Called to load a property.

## -parameters

### -param pHdr [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that identifies the property to load. This structure contains the same data as the structure passed to <a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize</a>.

### -param ppStream [out]

Pointer to an <b>IStream</b> interface pointer that receives the stream object.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

Only property data is written to the stream. The header data is not written to the stream.

Obtain the original position of the stream before writing to the stream. The original position should be restored in the stream before returning from this method.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp">ITfPersistentPropertyLoaderACP</a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>