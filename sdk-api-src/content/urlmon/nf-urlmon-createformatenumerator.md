---
UID: NF:urlmon.CreateFormatEnumerator
title: CreateFormatEnumerator function (urlmon.h)
description: Creates an object that implements IEnumFORMATETC over a static array of FORMATETC structures.
helpviewer_keywords: ["CreateFormatEnumerator","CreateFormatEnumerator function [COM]","_ole_CreateFormatEnumerator","com.createformatenumerator","urlmon/CreateFormatEnumerator"]
old-location: com\createformatenumerator.htm
tech.root: com
ms.assetid: 302418e5-48b6-46ee-bb96-2a8170c4af5e
ms.date: 12/05/2018
ms.keywords: CreateFormatEnumerator, CreateFormatEnumerator function [COM], _ole_CreateFormatEnumerator, com.createformatenumerator, urlmon/CreateFormatEnumerator
req.header: urlmon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Urlmon.lib
req.dll: Urlmon.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateFormatEnumerator
 - urlmon/CreateFormatEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Urlmon.dll
api_name:
 - CreateFormatEnumerator
---

# CreateFormatEnumerator function


## -description

Creates an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> over a static array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures.

## -parameters

### -param cfmtetc [in]

Number of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures in the static array specified by the <i>rgfmtetc</i> parameter. The <i>cfmtetc</i> parameter cannot be zero.

### -param rgfmtetc [in]

Pointer to a static array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures.

### -param ppenumfmtetc [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the enumerator object.

## -returns

This function returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

The <b>CreateFormatEnumerator</b> function creates an enumerator object that implements <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> over a static array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures. The <i>cfmtetc</i> parameter specifies the number of these structures. With the pointer, you can call the standard enumeration methods to enumerate the structures.