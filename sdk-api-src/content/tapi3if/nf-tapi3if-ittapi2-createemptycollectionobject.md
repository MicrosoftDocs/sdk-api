---
UID: NF:tapi3if.ITTAPI2.CreateEmptyCollectionObject
title: ITTAPI2::CreateEmptyCollectionObject
author: windows-sdk-content
description: The CreateEmptyCollectionObject method creates an empty collection object. The collection can be filled with ITDetectTone or ITCustomTone objects for use with the DetectTonesByCollection method or the GenerateCustomTonesByCollection method, respectively.
old-location: tapi3\ittapi2_createemptycollectionobject.htm
old-project: tapi
ms.assetid: 0114c0d2-4582-4b44-8fb6-74e468828797
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CreateEmptyCollectionObject, CreateEmptyCollectionObject method [TAPI 2.2], CreateEmptyCollectionObject method [TAPI 2.2],ITTAPI2 interface, ITTAPI2 interface [TAPI 2.2],CreateEmptyCollectionObject method, ITTAPI2.CreateEmptyCollectionObject, ITTAPI2::CreateEmptyCollectionObject, _tapi3_ittapi2_createemptycollectionobject, tapi3.ittapi2_createemptycollectionobject, tapi3if/ITTAPI2::CreateEmptyCollectionObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI2.CreateEmptyCollectionObject
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI2::CreateEmptyCollectionObject


## -description


The 
<b>CreateEmptyCollectionObject</b> method creates an empty collection object. The collection can be filled with 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> or 
<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a> objects for use with the 
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a> method or the 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a> method, respectively.

This method is intended for Visual Basic and scripting applications.


## -parameters




### -param ppCollection [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a> interface on the new collection object.


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




<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a>



<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/8c67f31e-783e-4371-9f17-063f8ecfc069">ITTAPI2</a>
 

 

