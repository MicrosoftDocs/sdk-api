---
UID: NF:msctf.ITfCreatePropertyStore.CreatePropertyStore
title: ITfCreatePropertyStore::CreatePropertyStore
author: windows-driver-content
description: ITfCreatePropertyStore::CreatePropertyStore method
old-location: tsf\itfcreatepropertystore_createpropertystore.htm
old-project: TSF
ms.assetid: 8c2e612c-31d8-4c89-97c4-3e248d7b7b28
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore method [Text Services Framework], CreatePropertyStore method [Text Services Framework],ITfCreatePropertyStore interface, ITfCreatePropertyStore interface [Text Services Framework],CreatePropertyStore method, ITfCreatePropertyStore.CreatePropertyStore, ITfCreatePropertyStore::CreatePropertyStore, _tsf_itfcreatepropertystore_createpropertystore_ref, msctf/ITfCreatePropertyStore::CreatePropertyStore, tsf.itfcreatepropertystore_createpropertystore
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tiptsf.dll
api_name:
-	ITfCreatePropertyStore.CreatePropertyStore
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCreatePropertyStore::CreatePropertyStore


## -description




## -parameters




### -param guidProp [in]

Contains the type identifier of the property. For more information, see <a href="https://msdn.microsoft.com/e0b6b1b7-1994-4876-9f15-7e1c6a4f0e4b">ITfPropertyStore::GetType</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that contains the text to be covered by the property store.


### -param cb [in]

Contains the size, in bytes, of the property store data contained in <i>pStream</i>.


### -param pStream [in]

Pointer to an <b>IStream</b> object that contains the property store data.


### -param ppStore [out]

Pointer to an <a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a> interface pointer that receives the property store object created by this method.


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
 

 

