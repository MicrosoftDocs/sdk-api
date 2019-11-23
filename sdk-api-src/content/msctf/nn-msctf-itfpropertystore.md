---
UID: NN:msctf.ITfPropertyStore
title: ITfPropertyStore (msctf.h)

description: The ITfPropertyStore interface is implemented by a text service and used by the TSF manager to provide non-static property values. An instance of this interface is passed to ITfProperty::SetValueStore.
old-location: tsf\itfpropertystore.htm
tech.root: TSF
ms.assetid: 0678e622-3733-499b-b289-c8c181d4638c

ms.date: 12/05/2018
ms.keywords: ITfPropertyStore, ITfPropertyStore interface [Text Services Framework], ITfPropertyStore interface [Text Services Framework],described, _tsf_itfpropertystore_ref, msctf/ITfPropertyStore, tsf.itfpropertystore
ms.topic: interface
f1_keywords: 
 - "msctf/ITfPropertyStore"
dev_langs:
 - c++
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
 - msctf.dll
api_name:
 - ITfPropertyStore
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfPropertyStore interface


## -description


The <b>ITfPropertyStore</b> interface is implemented by a text service and used by the TSF manager to provide non-static property values. An instance of this interface is passed to <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-setvaluestore">ITfProperty::SetValueStore</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPropertyStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an exact copy of the property store object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-divide">Divide</a>
</td>
<td align="left" width="63%">
Called when the text covered by the property is split into two ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-getdata">GetData</a>
</td>
<td align="left" width="63%">
Obtains the property store data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-getdatatype">GetDataType</a>
</td>
<td align="left" width="63%">
This method is reserved, but must be implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-getpropertyrangecreator">GetPropertyRangeCreator</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the property store owner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-gettype">GetType</a>
</td>
<td align="left" width="63%">
Obtains the property identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-ontextupdated">OnTextUpdated</a>
</td>
<td align="left" width="63%">
Called when the text that the property store applies to is modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Called to write the property store data into a stream for serialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpropertystore-shrink">Shrink</a>
</td>
<td align="left" width="63%">
Called when the text that the property store applies to is truncated.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfproperty-setvaluestore">ITfProperty::SetValueStore
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

