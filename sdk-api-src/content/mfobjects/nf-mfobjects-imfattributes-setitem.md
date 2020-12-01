---
UID: NF:mfobjects.IMFAttributes.SetItem
title: IMFAttributes::SetItem (mfobjects.h)
description: Adds an attribute value with a specified key.
helpviewer_keywords: ["1ac6e1c3-cf78-4cff-a992-4f92f243c443","IMFAttributes interface [Media Foundation]","SetItem method","IMFAttributes.SetItem","IMFAttributes::SetItem","SetItem","SetItem method [Media Foundation]","SetItem method [Media Foundation]","IMFAttributes interface","mf.imfattributes_setitem","mfobjects/IMFAttributes::SetItem"]
old-location: mf\imfattributes_setitem.htm
tech.root: mf
ms.assetid: 1ac6e1c3-cf78-4cff-a992-4f92f243c443
ms.date: 12/05/2018
ms.keywords: 1ac6e1c3-cf78-4cff-a992-4f92f243c443, IMFAttributes interface [Media Foundation],SetItem method, IMFAttributes.SetItem, IMFAttributes::SetItem, SetItem, SetItem method [Media Foundation], SetItem method [Media Foundation],IMFAttributes interface, mf.imfattributes_setitem, mfobjects/IMFAttributes::SetItem
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
 - IMFAttributes::SetItem
 - mfobjects/IMFAttributes::SetItem
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
 - IMFAttributes.SetItem
---

# IMFAttributes::SetItem


## -description

Adds an attribute value with a specified key.

## -parameters

### -param guidKey [in]

A GUID that identifies the value to set. If this key already exists, the method overwrites the old value.

### -param Value [in]

A <b>PROPVARIANT</b> that contains the attribute value. The method copies the value. The <b>PROPVARIANT</b> type must be one of the types listed in the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a> enumeration.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
Invalid attribute type.
              

</td>
</tr>
</table>

## -remarks

This method checks whether the <b>PROPVARIANT</b> type is one of the attribute types defined in <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>, and fails if an unsupported type is used. However, this method does not check whether the <b>PROPVARIANT</b> is the correct type for the specified attribute GUID. (There is no programmatic way to associate attribute GUIDs with property types.) For a list of Media Foundation attributes and their data types, see <a href="/windows/desktop/medfound/media-foundation-attributes">Media Foundation Attributes</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>