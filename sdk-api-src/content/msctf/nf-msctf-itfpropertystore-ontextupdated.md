---
UID: NF:msctf.ITfPropertyStore.OnTextUpdated
title: ITfPropertyStore::OnTextUpdated (msctf.h)
description: ITfPropertyStore::OnTextUpdated method
helpviewer_keywords: ["ITfPropertyStore interface [Text Services Framework]","OnTextUpdated method","ITfPropertyStore.OnTextUpdated","ITfPropertyStore::OnTextUpdated","OnTextUpdated","OnTextUpdated method [Text Services Framework]","OnTextUpdated method [Text Services Framework]","ITfPropertyStore interface","TF_TU_CORRECTION","_tsf_itfpropertystore_ontextupdated_ref","msctf/ITfPropertyStore::OnTextUpdated","tsf.itfpropertystore_ontextupdated"]
old-location: tsf\itfpropertystore_ontextupdated.htm
tech.root: TSF
ms.assetid: 6e3d6341-6e5b-445e-b6ac-48853a5b56f2
ms.date: 12/05/2018
ms.keywords: ITfPropertyStore interface [Text Services Framework],OnTextUpdated method, ITfPropertyStore.OnTextUpdated, ITfPropertyStore::OnTextUpdated, OnTextUpdated, OnTextUpdated method [Text Services Framework], OnTextUpdated method [Text Services Framework],ITfPropertyStore interface, TF_TU_CORRECTION, _tsf_itfpropertystore_ontextupdated_ref, msctf/ITfPropertyStore::OnTextUpdated, tsf.itfpropertystore_ontextupdated
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfPropertyStore::OnTextUpdated
 - msctf/ITfPropertyStore::OnTextUpdated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfPropertyStore.OnTextUpdated
---

# ITfPropertyStore::OnTextUpdated


## -description

Called when the text that the property store applies to is modified.

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

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the range of text modified.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>