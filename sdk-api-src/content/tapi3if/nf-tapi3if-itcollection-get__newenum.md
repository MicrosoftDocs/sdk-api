---
UID: NF:tapi3if.ITCollection.get__NewEnum
title: ITCollection::get__NewEnum (tapi3if.h)
description: The get__NewEnum method gets an enumerator for the collection.
helpviewer_keywords: ["ITCollection interface [TAPI 2.2]","get__NewEnum method","ITCollection.get__NewEnum","ITCollection::get__NewEnum","_tapi3_itcollection_get__newenum","get__NewEnum","get__NewEnum method [TAPI 2.2]","get__NewEnum method [TAPI 2.2]","ITCollection interface","tapi3.itcollection_get__newenum","tapi3if/ITCollection::get__NewEnum"]
old-location: tapi3\itcollection_get__newenum.htm
tech.root: tapi3
ms.assetid: 4b84298f-f114-4171-a2ad-d14122cb4bc8
ms.date: 12/05/2018
ms.keywords: ITCollection interface [TAPI 2.2],get__NewEnum method, ITCollection.get__NewEnum, ITCollection::get__NewEnum, _tapi3_itcollection_get__newenum, get__NewEnum, get__NewEnum method [TAPI 2.2], get__NewEnum method [TAPI 2.2],ITCollection interface, tapi3.itcollection_get__newenum, tapi3if/ITCollection::get__NewEnum
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCollection::get__NewEnum
 - tapi3if/ITCollection::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCollection.get__NewEnum
---

# ITCollection::get__NewEnum


## -description

The 
<b>get__NewEnum</b> method gets an enumerator for the collection.

## -parameters

### -param ppNewEnum [out]

Pointer to an 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on an enumerator object for the collection. 




Call the 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the returned <b>IUnknown</b> interface to obtain a pointer to an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> enumeration interface on the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection.

For more information, see the following Remarks section.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

Each TAPI 3 interface that includes a method that returns a collection also includes a method that returns a pointer to a TAPI 3 enumerator interface. If you are programming in C/C++, it can be easier to call a collection's enumerator method directly to obtain an enumerator object, instead of calling the <b>ITCollection::get__NewEnum</b> method. For example, the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses">ITTAPI::EnumerateAddresses</a> method returns a pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface. 
<b>IEnumAddress</b> provides enumeration methods for the 
<a href="/windows/desktop/Tapi/address-object">Address object</a>.

If you are programming in Visual Basic, you do not need to call this method to enumerate a collection. This is because you can invoke the method's functionality implicitly using the <b>For...Each...in...Next...</b> construct.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>