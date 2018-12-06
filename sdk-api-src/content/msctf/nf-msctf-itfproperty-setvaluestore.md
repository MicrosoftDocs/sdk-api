---
UID: NF:msctf.ITfProperty.SetValueStore
title: ITfProperty::SetValueStore
author: windows-sdk-content
description: ITfProperty::SetValueStore method
old-location: tsf\itfproperty_setvaluestore.htm
tech.root: TSF
ms.assetid: 146af429-54a8-41b6-b44e-b5d35f933435
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfProperty interface [Text Services Framework],SetValueStore method, ITfProperty.SetValueStore, ITfProperty::SetValueStore, SetValueStore, SetValueStore method [Text Services Framework], SetValueStore method [Text Services Framework],ITfProperty interface, _tsf_itfproperty_setvaluestore_ref, msctf/ITfProperty::SetValueStore, tsf.itfproperty_setvaluestore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfProperty.SetValueStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfProperty::SetValueStore


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the range that the property value is set for. This parameter cannot be <b>NULL</b>. This method fails if <i>pRange</i> is empty.


### -param pPropStore [in]

Pointer to an <a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a> interface that obtains the property data.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read/write lock.

</td>
</tr>
</table>
 




## -remarks



Property values set with <a href="https://msdn.microsoft.com/72064f9f-311e-4d7b-9ead-4fe2b7f528a8">ITfProperty::SetValue</a> will be discarded when the text that the property value covers is modified. To gain control over what happens to a property value when the text is modified, use <b>ITfProperty::SetValueStore</b> .

Values set with <b>ITfProperty::SetValue</b> will be serialized, except for values of type VT_UNKNOWN, which are not serialized. If a property value of type VT_UNKNOWN must be serialized, use <b>ITfProperty::SetValueStore</b> instead.

Overlapping property values of the same type are unsupported.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a>



<a href="https://msdn.microsoft.com/72064f9f-311e-4d7b-9ead-4fe2b7f528a8">ITfProperty::SetValue
      </a>



<a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

