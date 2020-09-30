---
UID: NF:propsys.IPropertyStore.SetValue
title: IPropertyStore::SetValue (propsys.h)
description: This method sets a property value or replaces or removes an existing value.
helpviewer_keywords: ["IPropertyStore interface [Audio Devices]","SetValue method","IPropertyStore.SetValue","IPropertyStore::SetValue","SetValue","SetValue (IpropertyStore)","SetValue method [Audio Devices]","SetValue method [Audio Devices]","IPropertyStore interface","audio.ipropertystore_setvalue","audio_syseffects_r_0f840b2a-35e2-4a93-9c50-84671d662b7d.xml","propsys/IPropertyStore::SetValue"]
old-location: audio\ipropertystore_setvalue.htm
tech.root: audio
ms.assetid: be21bcb2-6875-4559-abd7-a496f0fcddd6
ms.date: 12/05/2018
ms.keywords: IPropertyStore interface [Audio Devices],SetValue method, IPropertyStore.SetValue, IPropertyStore::SetValue, SetValue, SetValue (IpropertyStore), SetValue method [Audio Devices], SetValue method [Audio Devices],IPropertyStore interface, audio.ipropertystore_setvalue, audio_syseffects_r_0f840b2a-35e2-4a93-9c50-84671d662b7d.xml, propsys/IPropertyStore::SetValue
req.header: propsys.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStore::SetValue
 - propsys/IPropertyStore::SetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.idl
 - Propsys.idl.dll
api_name:
 - IPropertyStore.SetValue
---

# IPropertyStore::SetValue


## -description

This method sets a property value or replaces or removes an existing value.

## -parameters

### -param key

TBD

### -param propvar

TBD

### -param Key

A reference to the PROPERTYKEY structure that is retrieved through <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>. This structure contains a global unique identifier (GUID) for the property.


#### - pv

A pointer to a <a href="/previous-versions/aa912007(v=msdn.10)">PROPVARIANT</a> structure that contains the new property data.

## -returns

The <code>IPropertyStore::SetValue</code> method can return any one of the following:

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
The property change was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The value was set but truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This is an error code. The property store was read-only so the method was not able to set the value.

</td>
</tr>
</table>

## -remarks

<code>IPropertyStore::SetValue</code> affects the current property store instance only. A property handler implements <code>IPropertyStore::SetValue</code> by accumulating property changes in an in-memory data structure. Property changes are written to the stream only when <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> is called.

If <b>IPropertyStore::Commit</b> is called on a read-only property store, the property handler determines this and returns STG_E_ACCESSDENIED.

If a value was added or removed as a result of <code>SetValue</code>, subsequent enumerations by <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getcount">IPropertyStore::GetCount</a> and <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a> reflect that change and subsequent calls to <code>IPropertyStore::SetValue</code> reflect the changed value.

<b>Adding a New Property</b>

If the property value that was pointed to by key does not exist in the store, <code>IPropertyStore::SetValue</code> adds the value to the store.

<b>Replacing an Existing Property Value</b>

If the property value that was pointed to by key already exists in the store, the stored value is replaced.

<b>Removing an Existing Property</b>

To remove a value from the property store, set the vt member of the structure that is pointed to by pv to VT_EMPTY. If that value is not present, do nothing and the method returns S_OK.

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>



<a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getcount">IPropertyStore::GetCount</a>