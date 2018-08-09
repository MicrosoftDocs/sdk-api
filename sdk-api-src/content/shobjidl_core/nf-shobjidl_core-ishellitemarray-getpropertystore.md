---
UID: NF:shobjidl_core.IShellItemArray.GetPropertyStore
title: IShellItemArray::GetPropertyStore
author: windows-sdk-content
description: Gets a property store.
old-location: shell\IShellItemArray_GetPropertyStore.htm
old-project: shell
ms.assetid: 138a604f-e8dd-48ee-9678-a0530c1a16f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPropertyStore, GetPropertyStore method [Windows Shell], GetPropertyStore method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetPropertyStore method, IShellItemArray.GetPropertyStore, IShellItemArray::GetPropertyStore, _shell_IShellItemArray_GetPropertyStore, shell.IShellItemArray_GetPropertyStore, shobjidl_core/IShellItemArray::GetPropertyStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray.GetPropertyStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItemArray::GetPropertyStore


## -description


Gets a property store.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a> constants.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains interface pointer requested in riid.  This is typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or <a href="https://msdn.microsoft.com/b4e51201-47af-449f-9050-aec3207320f5">IPropertyStoreCapabilities</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used to obtain a read-only property store that aggregates properties gathered from all the items in the shell item array.

If there is more than one item in the shell item array, then the resulting property store will aggregate the values from each item according to a set of rules determined by each property.   Values read from the property store will be coerced to a canonical form prior to aggregation as discussed at <a href="https://msdn.microsoft.com/bc51ec1b-c1ec-4162-a60d-b67d19d5b591">CoerceToCanonicalValue</a>.  The output from a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> is computed as follows:

<ul>
<li>Single valued properties follow the rule specified by the <a href="https://msdn.microsoft.com/ae1f8835-ef6c-42bb-b44f-ad374337a012">aggregation type</a> string in the property description schema.</li>
<li>
<ul>
<li>If the aggregation type is "DateRange" and the property type is a filetime, returns a VT_VECTOR | VT_FILETIME of two values, or a VT_FILETIME value if the values were identical.</li>
<li>If the aggregation type is "First", returns the first non-empty value.</li>
<li>If the aggregation type is "Sum", returns the sum.</li>
<li>If the aggregation type is "Average", returns the average of all non-empty values.</li>
<li>If the aggregation type is "Minimum", returns the minimum value.</li>
<li>If the aggregation type is "Union" and the property type is a string, returns a VT_VECTOR | VT_LPWSTR containing the union of values.  The order of the values is unspecified.</li>
<li>If the aggregation type is unspecified, incompatible, or "Default", either returns a single value if it is identical for all items in the array, or a special value used to indicate that the values differ between some of the items.  The special value is a VT_VECTOR | VT_LPWSTR containing two strings: "Multiple" and "Values".  Calling applications should check for this special value by checking for VT_VECTOR | VT_LPWSTR if <a href="https://msdn.microsoft.com/20ff02c1-72de-479f-afd8-29ec580bbfcb">GetTypeFlags</a> indicates the property is single-valued.</li>
</ul>
</li>
<li>Multi-valued string properties return an intersection of their strings.  The order is unspecified.</li>
</ul>
Calls to <a href="https://msdn.microsoft.com/ffd13c93-3011-4955-ad1e-2731afd83956">IsPropertyWritable</a> will return S_FALSE only if all the items have property handlers that implement <a href="https://msdn.microsoft.com/b4e51201-47af-449f-9050-aec3207320f5">IPropertyStoreCapabilities</a> and all the property stores indicate they do not support writing the property.

Calling applications may achieve other aggregation behaviors by accessing the individual shell items and their property stores directly.  See <a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>, and <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">GetPropertyStore</a>.

Writing to an array of shell items is supported via the <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> API.



