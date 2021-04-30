---
UID: NF:tapi3if.ITLegacyCallMediaControl2.DetectTonesByCollection
title: ITLegacyCallMediaControl2::DetectTonesByCollection (tapi3if.h)
description: The DetectTonesByCollection method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
helpviewer_keywords: ["DetectTonesByCollection","DetectTonesByCollection method [TAPI 2.2]","DetectTonesByCollection method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","DetectTonesByCollection method","ITLegacyCallMediaControl2.DetectTonesByCollection","ITLegacyCallMediaControl2::DetectTonesByCollection","_tapi3_itlegacycallmediacontrol2_detecttonesbycollection","tapi3.itlegacycallmediacontrol2_detecttonesbycollection","tapi3if/ITLegacyCallMediaControl2::DetectTonesByCollection"]
old-location: tapi3\itlegacycallmediacontrol2_detecttonesbycollection.htm
tech.root: tapi3
ms.assetid: 09cbcd9d-66cd-4131-b45c-cb3898d8446d
ms.date: 12/05/2018
ms.keywords: DetectTonesByCollection, DetectTonesByCollection method [TAPI 2.2], DetectTonesByCollection method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],DetectTonesByCollection method, ITLegacyCallMediaControl2.DetectTonesByCollection, ITLegacyCallMediaControl2::DetectTonesByCollection, _tapi3_itlegacycallmediacontrol2_detecttonesbycollection, tapi3.itlegacycallmediacontrol2_detecttonesbycollection, tapi3if/ITLegacyCallMediaControl2::DetectTonesByCollection
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
 - ITLegacyCallMediaControl2::DetectTonesByCollection
 - tapi3if/ITLegacyCallMediaControl2::DetectTonesByCollection
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
 - ITLegacyCallMediaControl2.DetectTonesByCollection
---

# ITLegacyCallMediaControl2::DetectTonesByCollection


## -description

The 
<b>DetectTonesByCollection</b> method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttones">DetectTones</a> method instead.

## -parameters

### -param pDetectToneCollection [in]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a> interface containing a collection of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a> interface pointers that represent the tones to monitor. Each tone in the list has an application-defined tag field that is used to identify the individual tones when tone detection is reported by a <b>TE_TONEEVENT</b> event. For more information, see the following Remarks section.

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
The <i>pDetectToneCollection</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the tones buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call must be in the <i>connected</i> state.

</td>
</tr>
</table>

## -remarks

This method translates to a TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-linemonitortones">lineMonitorTones</a> call.

To cancel tone monitoring in progress, call the 
<b>DetectTonesByCollection</b> method and specify an empty collection. To change the list of tones to monitor, call this method and specify a new tone collection.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>