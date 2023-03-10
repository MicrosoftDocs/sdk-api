---
UID: NF:shobjidl_core.IShellItemArray.GetPropertyStore
title: IShellItemArray::GetPropertyStore (shobjidl_core.h)
description: Gets a property store.
helpviewer_keywords: ["GetPropertyStore","GetPropertyStore method [Windows Shell]","GetPropertyStore method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","GetPropertyStore method","IShellItemArray.GetPropertyStore","IShellItemArray::GetPropertyStore","_shell_IShellItemArray_GetPropertyStore","shell.IShellItemArray_GetPropertyStore","shobjidl_core/IShellItemArray::GetPropertyStore"]
old-location: shell\IShellItemArray_GetPropertyStore.htm
tech.root: shell
ms.assetid: 138a604f-e8dd-48ee-9678-a0530c1a16f2
ms.date: 12/05/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Shell], GetPropertyStore method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetPropertyStore method, IShellItemArray.GetPropertyStore, IShellItemArray::GetPropertyStore, _shell_IShellItemArray_GetPropertyStore, shell.IShellItemArray_GetPropertyStore, shobjidl_core/IShellItemArray::GetPropertyStore
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IShellItemArray::GetPropertyStore
 - shobjidl_core/IShellItemArray::GetPropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray.GetPropertyStore
---

# IShellItemArray::GetPropertyStore


## -description

Gets a property store.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

One of the <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> constants.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains interface pointer requested in riid.  This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to obtain a read-only property store that aggregates properties gathered from all the items in the shell item array.

If there is more than one item in the shell item array, then the resulting property store will aggregate the values from each item according to a set of rules determined by each property.   Values read from the property store will be coerced to a canonical form prior to aggregation as discussed at <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-coercetocanonicalvalue">CoerceToCanonicalValue</a>.  The output from a call to <a href="/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)">IPropertyStore::GetValue</a> is computed as follows:

<ul>
<li>Single valued properties follow the rule specified by the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">aggregation type</a> string in the property description schema.</li>
<li>
<ul>
<li>If the aggregation type is "DateRange" and the property type is a filetime, returns a VT_VECTOR | VT_FILETIME of two values, or a VT_FILETIME value if the values were identical.</li>
<li>If the aggregation type is "First", returns the first non-empty value.</li>
<li>If the aggregation type is "Sum", returns the sum.</li>
<li>If the aggregation type is "Average", returns the average of all non-empty values.</li>
<li>If the aggregation type is "Minimum", returns the minimum value.</li>
<li>If the aggregation type is "Union" and the property type is a string, returns a VT_VECTOR | VT_LPWSTR containing the union of values.  The order of the values is unspecified.</li>
<li>If the aggregation type is unspecified, incompatible, or "Default", either returns a single value if it is identical for all items in the array, or a special value used to indicate that the values differ between some of the items.  The special value is a VT_VECTOR | VT_LPWSTR containing two strings: "Multiple" and "Values".  Calling applications should check for this special value by checking for VT_VECTOR | VT_LPWSTR if <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-gettypeflags">GetTypeFlags</a> indicates the property is single-valued.</li>
</ul>
</li>
<li>Multi-valued string properties return an intersection of their strings.  The order is unspecified.</li>
</ul>
Calls to <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable">IsPropertyWritable</a> will return S_FALSE only if all the items have property handlers that implement <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a> and all the property stores indicate they do not support writing the property.

Calling applications may achieve other aggregation behaviors by accessing the individual shell items and their property stores directly.  See <a href="/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)">IPropertyStore::GetCount</a>, <a href="/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)">IPropertyStore::GetAt</a>, and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">GetPropertyStore</a>.

Writing to an array of shell items is supported via the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> API.