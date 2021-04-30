---
UID: NF:tapi3if.ITTAPI2.CreateEmptyCollectionObject
title: ITTAPI2::CreateEmptyCollectionObject (tapi3if.h)
description: The CreateEmptyCollectionObject method creates an empty collection object. The collection can be filled with ITDetectTone or ITCustomTone objects for use with the DetectTonesByCollection method or the GenerateCustomTonesByCollection method, respectively.
helpviewer_keywords: ["CreateEmptyCollectionObject","CreateEmptyCollectionObject method [TAPI 2.2]","CreateEmptyCollectionObject method [TAPI 2.2]","ITTAPI2 interface","ITTAPI2 interface [TAPI 2.2]","CreateEmptyCollectionObject method","ITTAPI2.CreateEmptyCollectionObject","ITTAPI2::CreateEmptyCollectionObject","_tapi3_ittapi2_createemptycollectionobject","tapi3.ittapi2_createemptycollectionobject","tapi3if/ITTAPI2::CreateEmptyCollectionObject"]
old-location: tapi3\ittapi2_createemptycollectionobject.htm
tech.root: tapi3
ms.assetid: 0114c0d2-4582-4b44-8fb6-74e468828797
ms.date: 12/05/2018
ms.keywords: CreateEmptyCollectionObject, CreateEmptyCollectionObject method [TAPI 2.2], CreateEmptyCollectionObject method [TAPI 2.2],ITTAPI2 interface, ITTAPI2 interface [TAPI 2.2],CreateEmptyCollectionObject method, ITTAPI2.CreateEmptyCollectionObject, ITTAPI2::CreateEmptyCollectionObject, _tapi3_ittapi2_createemptycollectionobject, tapi3.ittapi2_createemptycollectionobject, tapi3if/ITTAPI2::CreateEmptyCollectionObject
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
 - ITTAPI2::CreateEmptyCollectionObject
 - tapi3if/ITTAPI2::CreateEmptyCollectionObject
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
 - ITTAPI2.CreateEmptyCollectionObject
---

# ITTAPI2::CreateEmptyCollectionObject


## -description

The 
<b>CreateEmptyCollectionObject</b> method creates an empty collection object. The collection can be filled with 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a> or 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a> objects for use with the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a> method or the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">GenerateCustomTonesByCollection</a> method, respectively.

This method is intended for Visual Basic and scripting applications.

## -parameters

### -param ppCollection [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a> interface on the new collection object.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCollection</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a>