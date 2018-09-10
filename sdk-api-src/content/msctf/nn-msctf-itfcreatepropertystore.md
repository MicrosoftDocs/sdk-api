---
UID: NN:msctf.ITfCreatePropertyStore
title: ITfCreatePropertyStore
author: windows-sdk-content
description: The ITfCreatePropertyStore interface is implemented by a text service to support persistence of property store data.
old-location: tsf\itfcreatepropertystore.htm
tech.root: TSF
ms.assetid: f21619c5-5f59-4cc4-9f84-fa5f8a178d40
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfCreatePropertyStore, ITfCreatePropertyStore interface [Text Services Framework], ITfCreatePropertyStore interface [Text Services Framework],described, _tsf_itfcreatepropertystore_ref, msctf/ITfCreatePropertyStore, tsf.itfcreatepropertystore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfCreatePropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCreatePropertyStore interface


## -description


The <b>ITfCreatePropertyStore</b> interface is implemented by a text service to support persistence of property store data. The TSF manager uses this interface to determine if a property store can be serialized and to create a property store object for a serialized property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCreatePropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCreatePropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCreatePropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c2e612c-31d8-4c89-97c4-3e248d7b7b28">CreatePropertyStore</a>
</td>
<td align="left" width="63%">
Creates a property store object from serialized property store data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5fdd81f-266b-4ff3-ab44-2d1c89a7aaea">IsStoreSerializable</a>
</td>
<td align="left" width="63%">
Determines if a property store can be stored as persistent data.

</td>
</tr>
</table> 


## -remarks



When a property store is unserialized, the TSF manager creates an object from the CLSID obtained from <a href="https://msdn.microsoft.com/e0b6b1b7-1994-4876-9f15-7e1c6a4f0e4b">ITfPropertyStore::GetPropertyRangeCreator</a> and obtain an <b>ITfCreatePropertyStore</b> interface pointer from it. The manager then uses <b>ITfCreatePropertyStore::CreatePropertyStore</b> to create the property store object.




## -see-also




<a href="https://msdn.microsoft.com/94fa2e8f-5bdd-4ec0-b632-269d4a7b3f73">ITfPropertyStore::GetPropertyRangeCreator
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

