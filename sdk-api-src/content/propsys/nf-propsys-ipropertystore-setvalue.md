---
UID: NF:propsys.IPropertyStore.SetValue
title: IPropertyStore::SetValue method
author: windows-driver-content
description: Sets a new property value, or replaces or removes an existing value.
old-location: properties\IPropertyStore_SetValue.htm
old-project: properties
ms.assetid: f5ede696-0cd4-41e2-9576-822e3f9909e7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IPropertyStore, IPropertyStore interface [Windows Properties], SetValue method, IPropertyStore::SetValue, SetValue method [Windows Properties], SetValue method [Windows Properties], IPropertyStore interface, SetValue,IPropertyStore.SetValue, properties.IPropertyStore_SetValue, propsys/IPropertyStore::SetValue, shell.IPropertyStore_SetValue, shell_IPropertyStore_SetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyStore.SetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPropertyStore::SetValue method


## -description


Sets a new property value, or replaces or removes an existing value.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure retrieved through <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>. This structure contains a unique identifier for the property in question.


### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the new property data.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b>  or INPLACE_S_TRUNCATED if successful or an error value otherwise. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The value was set but truncated in a string value or rounded if a numeric value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
 The property store was read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property handler could not store any value for the <a href="shell.PROPERTYKEY">PROPERTYKEY</a>  specified. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  When this method is implemented under <a href="shell.IPropertyStoreCache">IPropertyStoreCache</a>, be aware that the interface is used only by the in-memory store. Many of the following remarks may not apply in that case.</div>
<div> </div>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> affects the current property store instance only. A property handler implements <b>SetValue</b> by accumulating property changes in an in-memory data structure. Property changes are written to the stream only when <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> is called.

If <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> is called on a read-only property store, the property handler determines this and returns STG_E_ACCESSDENIED.

In general, errors should be detected and reported by <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>. However, when processing is deferred until <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> is called, the same error semantics apply.

If a value was added or removed as a result of <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>, subsequent enumerations by <a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> reflect that change and subsequent calls to <b>SetValue</b> reflect the changed value.

<h3><a id="Adding_a_New_Property"></a><a id="adding_a_new_property"></a><a id="ADDING_A_NEW_PROPERTY"></a>Adding a New Property</h3>
If the property value pointed to by key does not exist in the store, <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> adds the value to the store.

<h3><a id="Replacing_an_Existing_Property_Value"></a><a id="replacing_an_existing_property_value"></a><a id="REPLACING_AN_EXISTING_PROPERTY_VALUE"></a>Replacing an Existing Property Value</h3>
If the property value pointed to by the <i>key</i> parameter already exists in the store, the stored value is replaced.

<h3><a id="Removing_an_Existing_Property"></a><a id="removing_an_existing_property"></a><a id="REMOVING_AN_EXISTING_PROPERTY"></a>Removing an Existing Property</h3>
Removing a property values from a property store is not supported and could lead to unexpected results.

<h3><a id="Support_for_Different_Properties"></a><a id="support_for_different_properties"></a><a id="SUPPORT_FOR_DIFFERENT_PROPERTIES"></a>Support for Different Properties</h3>
A property handler must handle three types of properties in <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>: new properties introduced by the handler author, pre-existing properties that are germane to the property handler, and other properties that do not fall in either of those categories.

                

<ul>
<li>New properties introduced by the property handler author must be described in a property description XML file. Clients consume a file property handler through a wrapping layer called the Windows Property Provider. This layer delegates calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> to the property handler after it enforces restrictions on the new property according to the property description XML. Therefore, a handler should not attempt to enforce restrictions itself and must store any values that satisfy the property description XML. If the property description does not provide the necessary information to restrict values for the new property, the handler must alter the value as necessary to store those values successfully. For example, in the property description XML there is no way to specify that an integer-valued property can never be an odd number. If an odd integer were provided to <b>SetValue</b>, the handler is still required to store a value successfully. It could accomplish this by perhaps adding one to the value. If data is lost, <b>SetValue</b> must succeed with the return value INPLACE_S_TRUNCATED.</li>
<li>Pre-existing properties that are germane to the handler are those that have a representation in the handler's property storage format. For example, Adobe Acrobat .pdf files have representations for PKEY_Author and PKEY_Comments. These properties are described in a property description XML file provided by Windows. It is likely that the restrictions provided by Windows do not exactly match how the equivalent property must be stored in the author's file format. For example, the author value may be restricted to fewer characters in Acrobat files than in the property description for PKEY_Author. In this case, the handler author must make a best-effort attempt to coerce the property value. If data is lost, <a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a> must succeed with the return value INPLACE_S_TRUNCATED. In the unusual case that the value cannot be coerced, <b>SetValue</b> can return E_FAIL. If the author's file format is less restrictive than a property description provided by Windows, the Windows Property Provider layer described earlier will already have returned an error and therefore the property handler's <b>SetValue</b> will never be called to store the value.</li>
<li>Properties that are neither new nor pre-existing properties germane to the handler must still be stored by the property handler. The utility class CLSID_InMemoryPropertyStore, provided by Windows, can be used by handler authors to temporarily store such properties in memory and save those properties to a stream for storage in the file.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="shell.IPropertyStoreCache">IPropertyStoreCache</a>
 

 

