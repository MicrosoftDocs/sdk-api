---
UID: NF:tapi3if.ITLegacyCallMediaControl2.CreateDetectToneObject
title: ITLegacyCallMediaControl2::CreateDetectToneObject (tapi3if.h)
description: The CreateDetectToneObject method creates a detect tone object to use with the DetectTonesByCollection method.
helpviewer_keywords: ["CreateDetectToneObject","CreateDetectToneObject method [TAPI 2.2]","CreateDetectToneObject method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","CreateDetectToneObject method","ITLegacyCallMediaControl2.CreateDetectToneObject","ITLegacyCallMediaControl2::CreateDetectToneObject","_tapi3_itlegacycallmediacontrol2_createdetecttoneobject","tapi3.itlegacycallmediacontrol2_createdetecttoneobject","tapi3if/ITLegacyCallMediaControl2::CreateDetectToneObject"]
old-location: tapi3\itlegacycallmediacontrol2_createdetecttoneobject.htm
tech.root: tapi3
ms.assetid: 3f00391f-b63f-4fa7-82af-44584fbcd8a3
ms.date: 12/05/2018
ms.keywords: CreateDetectToneObject, CreateDetectToneObject method [TAPI 2.2], CreateDetectToneObject method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],CreateDetectToneObject method, ITLegacyCallMediaControl2.CreateDetectToneObject, ITLegacyCallMediaControl2::CreateDetectToneObject, _tapi3_itlegacycallmediacontrol2_createdetecttoneobject, tapi3.itlegacycallmediacontrol2_createdetecttoneobject, tapi3if/ITLegacyCallMediaControl2::CreateDetectToneObject
req.header: tapi3if.h
req.include-header: 
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
 - ITLegacyCallMediaControl2::CreateDetectToneObject
 - tapi3if/ITLegacyCallMediaControl2::CreateDetectToneObject
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
 - ITLegacyCallMediaControl2.CreateDetectToneObject
---

# ITLegacyCallMediaControl2::CreateDetectToneObject


## -description

The 
<b>CreateDetectToneObject</b> method creates a detect tone object to use with the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a> method.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttones">DetectTones</a> method instead.

## -parameters

### -param ppDetectTone [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a> interface.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppDetectTone</i> parameter is not a valid pointer.

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

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a> interface returned by <b>ITLegacyCallMediaControl2::CreateDetectToneObject</b>. The application must call the <b>Release</b> method on the 
<b>ITDetectTone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>