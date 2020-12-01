---
UID: NF:objidl.IMoniker.Hash
title: IMoniker::Hash (objidl.h)
description: Creates a hash value using the internal state of the moniker.
helpviewer_keywords: ["Hash","Hash method [COM]","Hash method [COM]","IMoniker interface","IMoniker interface [COM]","Hash method","IMoniker.Hash","IMoniker::Hash","_com_imoniker_hash","com.imoniker_hash","objidl/IMoniker::Hash"]
old-location: com\imoniker_hash.htm
tech.root: com
ms.assetid: 5073c909-d3bc-480e-97fb-d096e60787e5
ms.date: 12/05/2018
ms.keywords: Hash, Hash method [COM], Hash method [COM],IMoniker interface, IMoniker interface [COM],Hash method, IMoniker.Hash, IMoniker::Hash, _com_imoniker_hash, com.imoniker_hash, objidl/IMoniker::Hash
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMoniker::Hash
 - objidl/IMoniker::Hash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMoniker.Hash
---

# IMoniker::Hash


## -description

Creates a hash value using the internal state of the moniker.

## -parameters

### -param pdwHash [out]

A pointer to a variable that receives the hash value.

## -returns

This method returns S_OK to indicate that the hash value was retrieved successfully.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You can use the value returned by this method to maintain a hash table of monikers. The hash value determines a hash bucket in the table. To search such a table for a specified moniker, calculate its hash value and then compare it to the monikers in that hash bucket using <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isequal">IMoniker::IsEqual</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The hash value must be constant for the lifetime of the moniker. Two monikers that compare as equal using <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isequal">IMoniker::IsEqual</a> must hash to the same value.

Marshaling and then unmarshaling a moniker should have no effect on its hash value. Consequently, your implementation of <b>IMoniker::Hash</b> should rely only on the internal state of the moniker, not on its memory address.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method calculates a hash value for the moniker and returns S_OK. May return E_INVALIDARG if <i>pdwHash</i> is an invalid pointer.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method calculates a hash value for the moniker.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>Creates a hash value based on the URL string of the moniker. This hash value is identical when URL strings are identical, although it may also be identical for different URL strings. This method is used to speed up comparisons by reducing the amount of time that it is necessary to call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isequal">IMoniker::IsEqual</a>.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>