---
UID: NF:msctf.ITfCreatePropertyStore.IsStoreSerializable
title: ITfCreatePropertyStore::IsStoreSerializable
author: windows-sdk-content
description: ITfCreatePropertyStore::IsStoreSerializable method
old-location: tsf\itfcreatepropertystore_isstoreserializable.htm
old-project: TSF
ms.assetid: f5fdd81f-266b-4ff3-ab44-2d1c89a7aaea
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfCreatePropertyStore interface [Text Services Framework],IsStoreSerializable method, ITfCreatePropertyStore.IsStoreSerializable, ITfCreatePropertyStore::IsStoreSerializable, IsStoreSerializable, IsStoreSerializable method [Text Services Framework], IsStoreSerializable method [Text Services Framework],ITfCreatePropertyStore interface, _tsf_itfcreatepropertystore_isstoreserializable_ref, msctf/ITfCreatePropertyStore::IsStoreSerializable, tsf.itfcreatepropertystore_isstoreserializable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfCreatePropertyStore.IsStoreSerializable
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCreatePropertyStore::IsStoreSerializable


## -description




## -parameters




### -param guidProp [in]

Contains the type identifier of the property. For more information, see <a href="https://msdn.microsoft.com/e0b6b1b7-1994-4876-9f15-7e1c6a4f0e4b">ITfPropertyStore::GetType</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that contains the text covered by the property store.


### -param pPropStore [in]

Pointer to the <a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a> object.


### -param pfSerializable [out]

Pointer to a <b>BOOL</b> that receives a flag that indicates if the property store can be serialized. Receives nonzero if the property store can be serialized or zero otherwise.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f21619c5-5f59-4cc4-9f84-fa5f8a178d40">ITfCreatePropertyStore</a>



<a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore
      </a>



<a href="https://msdn.microsoft.com/e0b6b1b7-1994-4876-9f15-7e1c6a4f0e4b">
        ITfPropertyStore::GetType
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>
 

 

