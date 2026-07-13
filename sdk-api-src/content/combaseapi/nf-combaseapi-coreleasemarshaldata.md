---
UID: NF:combaseapi.CoReleaseMarshalData
title: CoReleaseMarshalData function (combaseapi.h)
description: Destroys a previously marshaled data packet.
helpviewer_keywords: ["CoReleaseMarshalData","CoReleaseMarshalData function [COM]","_com_CoReleaseMarshalData","com.coreleasemarshaldata","combaseapi/CoReleaseMarshalData"]
old-location: com\coreleasemarshaldata.htm
tech.root: com
ms.assetid: a642a20f-3a3c-46bc-b833-e424dab3a16d
ms.date: 12/05/2018
ms.keywords: CoReleaseMarshalData, CoReleaseMarshalData function [COM], _com_CoReleaseMarshalData, com.coreleasemarshaldata, combaseapi/CoReleaseMarshalData
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CoReleaseMarshalData
 - combaseapi/CoReleaseMarshalData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoReleaseMarshalData
---

# CoReleaseMarshalData function


## -description

Destroys a previously marshaled data packet.

## -parameters

### -param pStm [in]

A  pointer to the stream that contains the data packet to be destroyed. See <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -returns

This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The data packet was successfully destroyed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
An error related to the <i>pStm</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> function was not called on the current thread before this function was called.


</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data.

</div>
<div> </div>
The <b>CoReleaseMarshalData</b> function performs the following tasks:

<ol>
<li>The function reads a CLSID from the stream.</li>
<li>If COM's default marshaling implementation is being used, the function gets an <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer to an instance of the standard unmarshaler. If custom marshaling is being used, the function creates a proxy by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function, passing the CLSID it read from the stream, and requests an <b>IMarshal</b> interface pointer to the newly created proxy.</li>
<li>Using whichever <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> interface pointer it has acquired, the function calls <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-releasemarshaldata">IMarshal::ReleaseMarshalData</a>.</li>
</ol>
You typically do not call this function. The only situation in which you might need to call this function is if you use custom marshaling (write and use your own implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>). Examples of when <b>CoReleaseMarshalData</b> should be called include the following situations: 

<ul>
<li>
An attempt was made to unmarshal the data packet, but it failed.

</li>
<li>
A marshaled data packet was removed from a global table.

</li>
</ul>
As an analogy, the data packet can be thought of as a reference to the original object, just as if it were another interface pointer being held on the object. Like a real interface pointer, that data packet must be released at some point. The use of <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-releasemarshaldata">IMarshal::ReleaseMarshalData</a> to release data packets is analogous to the use of <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release interface pointers.

Note that you do not need to call <b>CoReleaseMarshalData</b> after a successful call of the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a> function; that function releases the marshal data as part of the processing that it does.


<div class="alert"><b>Important</b>  You must call  the <b>CoReleaseMarshalData</b> function in the same apartment that called <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a> to marshal the object into the stream. Failure to do this may cause the object reference held by the marshaled packet in the stream to be leaked.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imarshal-releasemarshaldata">IMarshal::ReleaseMarshalData</a>