---
UID: NN:mfobjects.IMFAttributes
title: IMFAttributes (mfobjects.h)
description: Provides a generic way to store key/value pairs on an object.
helpviewer_keywords: ["IMFAttributes","IMFAttributes interface [Media Foundation]","IMFAttributes interface [Media Foundation]","described","e12259f4-b631-4d4a-a296-c1cc6334b962","mf.imfattributes","mfobjects/IMFAttributes"]
old-location: mf\imfattributes.htm
tech.root: mf
ms.assetid: e12259f4-b631-4d4a-a296-c1cc6334b962
ms.date: 12/05/2018
ms.keywords: IMFAttributes, IMFAttributes interface [Media Foundation], IMFAttributes interface [Media Foundation],described, e12259f4-b631-4d4a-a296-c1cc6334b962, mf.imfattributes, mfobjects/IMFAttributes
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
 - IMFAttributes
 - mfobjects/IMFAttributes
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
 - IMFAttributes
---

# IMFAttributes interface


## -description

Provides a generic way to store key/value pairs on an object. The keys are <b>GUID</b>s, and the values can be any of the following data types: <b>UINT32</b>, <b>UINT64</b>, <b>double</b>, <b>GUID</b>, wide-character string, byte array, or <b>IUnknown</b> pointer. The standard implementation of this interface holds a thread lock while values are added, deleted, or retrieved.

For a list of predefined attribute <b>GUID</b>s, see <a href="/windows/desktop/medfound/media-foundation-attributes">Media Foundation Attributes</a>. Each attribute <b>GUID</b> has an expected data type. The various "set" methods in <b>IMFAttributes</b> do not validate the type against the attribute <b>GUID</b>. It is the application's responsibility to set the correct type for the attribute.

To create an empty attribute store, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAttributes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAttributes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAttributes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">Compare</a>
</td>
<td align="left" width="63%">
Compares the attributes on this object with the attributes on another object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compareitem">CompareItem</a>
</td>
<td align="left" width="63%">
Queries whether a stored attribute value equals a specified <b>PROPVARIANT</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems">CopyAllItems</a>
</td>
<td align="left" width="63%">
Copies all of the attributes from this object into another attribute store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-deleteallitems">DeleteAllItems</a>
</td>
<td align="left" width="63%">
Removes all key/value pairs from the object's attribute list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Removes a key/value pair from the object's attribute list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedblob">GetAllocatedBlob</a>
</td>
<td align="left" width="63%">
Retrieves a byte array associated with a key. This method allocates the memory for the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring">GetAllocatedString</a>
</td>
<td align="left" width="63%">
Retrieves a wide-character string associated with a key. This method allocates the memory for the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob">GetBlob</a>
</td>
<td align="left" width="63%">
Retrieves a byte array associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblobsize">GetBlobSize</a>
</td>
<td align="left" width="63%">
Retrieves the length of a byte array associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that are set on this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getdouble">GetDouble</a>
</td>
<td align="left" width="63%">
Retrieves a <b>double</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid">GetGUID</a>
</td>
<td align="left" width="63%">
Retrieves a <b>GUID</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getitembyindex">GetItemByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getitemtype">GetItemType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of the value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring">GetString</a>
</td>
<td align="left" width="63%">
Retrieves a wide-character string associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstringlength">GetStringLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of a string value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32">GetUINT32</a>
</td>
<td align="left" width="63%">
Retrieves a <b>UINT32</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">GetUINT64</a>
</td>
<td align="left" width="63%">
Retrieves a <b>UINT64</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown">GetUnknown</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-lockstore">LockStore</a>
</td>
<td align="left" width="63%">
Locks the attribute store so that no other thread can access it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob">SetBlob</a>
</td>
<td align="left" width="63%">
Associates a byte array with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setdouble">SetDouble</a>
</td>
<td align="left" width="63%">
Associates a <b>double</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid">SetGUID</a>
</td>
<td align="left" width="63%">
Associates a <b>GUID</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setitem">SetItem</a>
</td>
<td align="left" width="63%">
Associates an attribute value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring">SetString</a>
</td>
<td align="left" width="63%">
Associates a wide-character string with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32">SetUINT32</a>
</td>
<td align="left" width="63%">
Associates a <b>UINT32</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64">SetUINT64</a>
</td>
<td align="left" width="63%">
Associates a <b>UINT64</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown">SetUnknown</a>
</td>
<td align="left" width="63%">
Associates an <b>IUnknown</b> pointer with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-unlockstore">UnlockStore</a>
</td>
<td align="left" width="63%">
Unlocks the attribute store.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>