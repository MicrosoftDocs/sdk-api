---
UID: NF:msctf.ITfPropertyStore.GetPropertyRangeCreator
title: ITfPropertyStore::GetPropertyRangeCreator (msctf.h)
description: ITfPropertyStore::GetPropertyRangeCreator method
helpviewer_keywords: ["GetPropertyRangeCreator","GetPropertyRangeCreator method [Text Services Framework]","GetPropertyRangeCreator method [Text Services Framework]","ITfPropertyStore interface","ITfPropertyStore interface [Text Services Framework]","GetPropertyRangeCreator method","ITfPropertyStore.GetPropertyRangeCreator","ITfPropertyStore::GetPropertyRangeCreator","_tsf_itfpropertystore_getpropertyrangecreator_ref","msctf/ITfPropertyStore::GetPropertyRangeCreator","tsf.itfpropertystore_getpropertyrangecreator"]
old-location: tsf\itfpropertystore_getpropertyrangecreator.htm
tech.root: TSF
ms.assetid: 94fa2e8f-5bdd-4ec0-b632-269d4a7b3f73
ms.date: 12/05/2018
ms.keywords: GetPropertyRangeCreator, GetPropertyRangeCreator method [Text Services Framework], GetPropertyRangeCreator method [Text Services Framework],ITfPropertyStore interface, ITfPropertyStore interface [Text Services Framework],GetPropertyRangeCreator method, ITfPropertyStore.GetPropertyRangeCreator, ITfPropertyStore::GetPropertyRangeCreator, _tsf_itfpropertystore_getpropertyrangecreator_ref, msctf/ITfPropertyStore::GetPropertyRangeCreator, tsf.itfpropertystore_getpropertyrangecreator
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
 - ITfPropertyStore::GetPropertyRangeCreator
 - msctf/ITfPropertyStore::GetPropertyRangeCreator
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
 - ITfPropertyStore.GetPropertyRangeCreator
---

# ITfPropertyStore::GetPropertyRangeCreator


## -description

Obtains the class identifier of the property store owner.

## -parameters

### -param pclsid [out]

Pointer to a <b>CLSID</b> that receives the class identifier of the registered text service that implements <a href="/windows/desktop/api/msctf/nn-msctf-itfcreatepropertystore">ITfCreatePropertyStore</a>. The method can return CLSID_NULL for this parameter if property store persistence is unsupported.

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

When the property store is unserialized, the TSF manager creates an object of this CLSID and obtains an <b>ITfCreatePropertyStore</b> interface pointer from it. The manager then uses the <b>ITfCreatePropertyStore</b> object to create the property store object.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcreatepropertystore">ITfCreatePropertyStore
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a>