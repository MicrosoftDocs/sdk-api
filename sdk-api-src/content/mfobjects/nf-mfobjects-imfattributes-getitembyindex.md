---
UID: NF:mfobjects.IMFAttributes.GetItemByIndex
title: IMFAttributes::GetItemByIndex (mfobjects.h)
description: Retrieves an attribute at the specified index.
helpviewer_keywords: ["1290bc45-fcac-4379-b26c-e67ef678f193","GetItemByIndex","GetItemByIndex method [Media Foundation]","GetItemByIndex method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetItemByIndex method","IMFAttributes.GetItemByIndex","IMFAttributes::GetItemByIndex","mf.imfattributes_getitembyindex","mfobjects/IMFAttributes::GetItemByIndex"]
old-location: mf\imfattributes_getitembyindex.htm
tech.root: medfound
ms.assetid: 1290bc45-fcac-4379-b26c-e67ef678f193
ms.date: 12/05/2018
ms.keywords: 1290bc45-fcac-4379-b26c-e67ef678f193, GetItemByIndex, GetItemByIndex method [Media Foundation], GetItemByIndex method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetItemByIndex method, IMFAttributes.GetItemByIndex, IMFAttributes::GetItemByIndex, mf.imfattributes_getitembyindex, mfobjects/IMFAttributes::GetItemByIndex
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAttributes::GetItemByIndex
 - mfobjects/IMFAttributes::GetItemByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.GetItemByIndex
---

# IMFAttributes::GetItemByIndex


## -description

Retrieves an attribute at the specified index.

## -parameters

### -param unIndex [in]

Index of the attribute to retrieve. To get the number of attributes, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount">IMFAttributes::GetCount</a>.

### -param pguidKey [out]

Receives the GUID that identifies this attribute.

### -param pValue [in, out]

Pointer to a <b>PROPVARIANT</b> that receives the value. This parameter can be <b>NULL</b>. If it is not <b>NULL</b>, the method fills the <b>PROPVARIANT</b> with a copy of the attribute value. Call <b>PropVariantClear</b> to free the memory allocated by this method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index.

</td>
</tr>
</table>

## -remarks

To enumerate all of an object's attributes in a thread-safe way, do the following:

<ol>
<li>
Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-lockstore">IMFAttributes::LockStore</a> to prevent another thread from adding or deleting attributes.

</li>
<li>
Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount">IMFAttributes::GetCount</a> to find the number of attributes.

</li>
<li>
Call <b>GetItemByIndex</b> to get each attribute by index.

</li>
<li>
Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-unlockstore">IMFAttributes::UnlockStore</a> to unlock the attribute store.

</li>
</ol>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>