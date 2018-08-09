---
UID: NF:msctf.ITfPropertyStore.OnTextUpdated
title: ITfPropertyStore::OnTextUpdated
author: windows-sdk-content
description: ITfPropertyStore::OnTextUpdated method
old-location: tsf\itfpropertystore_ontextupdated.htm
old-project: TSF
ms.assetid: 6e3d6341-6e5b-445e-b6ac-48853a5b56f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfPropertyStore interface [Text Services Framework],OnTextUpdated method, ITfPropertyStore.OnTextUpdated, ITfPropertyStore::OnTextUpdated, OnTextUpdated, OnTextUpdated method [Text Services Framework], OnTextUpdated method [Text Services Framework],ITfPropertyStore interface, TF_TU_CORRECTION, _tsf_itfpropertystore_ontextupdated_ref, msctf/ITfPropertyStore::OnTextUpdated, tsf.itfpropertystore_ontextupdated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - msctf.dll
api_name:
 - ITfPropertyStore.OnTextUpdated
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPropertyStore::OnTextUpdated


## -description




## -parameters




### -param dwFlags [in]

Contains a set of flags that provide additional information about the text change. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TU_CORRECTION"></a><a id="tf_tu_correction"></a><dl>
<dt><b>TF_TU_CORRECTION</b></dt>
</dl>
</td>
<td width="60%">
The text change is the result of a correction. This implies that the semantics of the text have not changed. An example of this is when the spelling checker corrects a misspelled word.

</td>
</tr>
</table>
 


### -param pRangeNew [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the range of text modified.


### -param pfAccept [out]

Pointer to a <b>BOOL</b> variable that receives a value that indicates if the property store should be retained. Receives a nonzero value if the property store should be retained or zero if the property store should be discarded. If the property store is discarded, the TSF manager will set the property value to VT_EMPTY and release the property store.


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
 




## -remarks



If this method returns any value other than S_OK, the property store is discarded.




## -see-also




<a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

