---
UID: NF:msctf.ITfPropertyStore.Divide
title: ITfPropertyStore::Divide (msctf.h)
description: ITfPropertyStore::Divide method
helpviewer_keywords: ["Divide","Divide method [Text Services Framework]","Divide method [Text Services Framework]","ITfPropertyStore interface","ITfPropertyStore interface [Text Services Framework]","Divide method","ITfPropertyStore.Divide","ITfPropertyStore::Divide","_tsf_itfpropertystore_divide_ref","msctf/ITfPropertyStore::Divide","tsf.itfpropertystore_divide"]
old-location: tsf\itfpropertystore_divide.htm
tech.root: TSF
ms.assetid: 5b982cb1-e1b6-440b-9ac6-9b34bb86731d
ms.date: 12/05/2018
ms.keywords: Divide, Divide method [Text Services Framework], Divide method [Text Services Framework],ITfPropertyStore interface, ITfPropertyStore interface [Text Services Framework],Divide method, ITfPropertyStore.Divide, ITfPropertyStore::Divide, _tsf_itfpropertystore_divide_ref, msctf/ITfPropertyStore::Divide, tsf.itfpropertystore_divide
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
 - ITfPropertyStore::Divide
 - msctf/ITfPropertyStore::Divide
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
 - ITfPropertyStore.Divide
---

# ITfPropertyStore::Divide


## -description

Called when the text covered by the property is split into two ranges.

## -parameters

### -param pRangeThis [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the range that the property store now covers. This will be the range of text closest to the beginning of the context.

### -param pRangeNew [in]

Pointer to an <i>ITfRange</i> object that contains the range that the new property store will cover. This will be the range of text closest to the end of the context.

### -param ppPropStore [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a> interface pointer that receives a new property store object that will cover the range specified by <i>pRangeNew</i>.

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

This method creates a new property store object to cover <i>pRangeNew</i> and returns the pointer to this object in <i>ppPropStore</i>. If no new property store is returned, the original property store is discarded and the property store for both ranges is set to empty.

If this method returns any value other than S_OK, the original property store is discarded.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>