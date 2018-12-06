---
UID: NN:mfobjects.IMFAttributes
title: IMFAttributes
author: windows-sdk-content
description: Provides a generic way to store key/value pairs on an object.
old-location: mf\imfattributes.htm
tech.root: medfound
ms.assetid: e12259f4-b631-4d4a-a296-c1cc6334b962
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFAttributes, IMFAttributes interface [Media Foundation], IMFAttributes interface [Media Foundation],described, e12259f4-b631-4d4a-a296-c1cc6334b962, mf.imfattributes, mfobjects/IMFAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes interface


## -description


Provides a generic way to store key/value pairs on an object. The keys are <b>GUID</b>s, and the values can be any of the following data types: <b>UINT32</b>, <b>UINT64</b>, <b>double</b>, <b>GUID</b>, wide-character string, byte array, or <b>IUnknown</b> pointer. The standard implementation of this interface holds a thread lock while values are added, deleted, or retrieved.

For a list of predefined attribute <b>GUID</b>s, see <a href="https://msdn.microsoft.com/445fc879-3c9e-409d-8d05-ecd1ff9afc19">Media Foundation Attributes</a>. Each attribute <b>GUID</b> has an expected data type. The various "set" methods in <b>IMFAttributes</b> do not validate the type against the attribute <b>GUID</b>. It is the application's responsibility to set the correct type for the attribute.

To create an empty attribute store, call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAttributes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFAttributes</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1d0c9d1c-448d-4851-b183-94b04acb2ab5">Compare</a>
</td>
<td align="left" width="63%">
Compares the attributes on this object with the attributes on another object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0a6073b-fce6-4a1f-b7d1-ef6543e7648f">CompareItem</a>
</td>
<td align="left" width="63%">
Queries whether a stored attribute value equals a specified <b>PROPVARIANT</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/111b55bc-fb8e-45b5-a709-703acd23c4be">CopyAllItems</a>
</td>
<td align="left" width="63%">
Copies all of the attributes from this object into another attribute store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d7ef03b-bb96-42bc-a1c3-49f8b0e499b8">DeleteAllItems</a>
</td>
<td align="left" width="63%">
Removes all key/value pairs from the object's attribute list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac72e6e4-f930-4de6-92a2-f15e5f9e5d74">DeleteItem</a>
</td>
<td align="left" width="63%">
Removes a key/value pair from the object's attribute list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/380e0e3a-b5c5-4d31-8793-417262377fef">GetAllocatedBlob</a>
</td>
<td align="left" width="63%">
Retrieves a byte array associated with a key. This method allocates the memory for the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/550a3035-ea16-4784-8f69-9522259bb338">GetAllocatedString</a>
</td>
<td align="left" width="63%">
Retrieves a wide-character string associated with a key. This method allocates the memory for the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68528db7-90df-4abe-a957-ffb8c3f12cef">GetBlob</a>
</td>
<td align="left" width="63%">
Retrieves a byte array associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93ab65e7-2168-4cfb-a871-b39554ba66e0">GetBlobSize</a>
</td>
<td align="left" width="63%">
Retrieves the length of a byte array associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f511d5c-249c-4311-8380-a932a755eaaf">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that are set on this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/650a5f7f-609f-477b-8834-ff66ca3a9ca3">GetDouble</a>
</td>
<td align="left" width="63%">
Retrieves a <b>double</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ded35e1-2d1c-4e68-ad0f-2bd5ba469853">GetGUID</a>
</td>
<td align="left" width="63%">
Retrieves a <b>GUID</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cc4e529-d5a0-4342-82ac-ae5b28bfd61d">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1290bc45-fcac-4379-b26c-e67ef678f193">GetItemByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c3a3c30-da10-4365-9f76-598a4ca7675c">GetItemType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of the value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/756d8fba-d372-46f9-8035-f657d7ff133f">GetString</a>
</td>
<td align="left" width="63%">
Retrieves a wide-character string associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ccc753f-e147-47f4-ab95-17687729404a">GetStringLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of a string value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e47495e0-3274-4ce2-9fd3-d2fb2afb7578">GetUINT32</a>
</td>
<td align="left" width="63%">
Retrieves a <b>UINT32</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3240fff-48d8-4d88-8c75-15f00bfe72ed">GetUINT64</a>
</td>
<td align="left" width="63%">
Retrieves a <b>UINT64</b> value associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5f645a1-b7d2-47d3-b77e-ad94815b1c25">GetUnknown</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer associated with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ec7aed3-7dbc-4aa4-92d5-646aee757db7">LockStore</a>
</td>
<td align="left" width="63%">
Locks the attribute store so that no other thread can access it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a2a25a9-4dea-40c8-988c-9e3806c8f31c">SetBlob</a>
</td>
<td align="left" width="63%">
Associates a byte array with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb58f35e-0fca-4b19-9976-de2140e6ebc0">SetDouble</a>
</td>
<td align="left" width="63%">
Associates a <b>double</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d73b53f5-4a8f-4903-986d-fbf4277a2d45">SetGUID</a>
</td>
<td align="left" width="63%">
Associates a <b>GUID</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ac6e1c3-cf78-4cff-a992-4f92f243c443">SetItem</a>
</td>
<td align="left" width="63%">
Associates an attribute value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51d2a2a0-92cb-49e0-b4a9-7201e9d92322">SetString</a>
</td>
<td align="left" width="63%">
Associates a wide-character string with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c30fd56-719f-4831-8fbf-cefcf9d72709">SetUINT32</a>
</td>
<td align="left" width="63%">
Associates a <b>UINT32</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">SetUINT64</a>
</td>
<td align="left" width="63%">
Associates a <b>UINT64</b> value with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0c3d59-07c4-4431-a137-8655ddbf6258">SetUnknown</a>
</td>
<td align="left" width="63%">
Associates an <b>IUnknown</b> pointer with a key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65e35864-868a-4ae9-86ed-772a2b2daeb6">UnlockStore</a>
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




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

