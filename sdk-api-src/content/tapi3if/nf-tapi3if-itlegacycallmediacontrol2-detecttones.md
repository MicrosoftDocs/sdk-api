---
UID: NF:tapi3if.ITLegacyCallMediaControl2.DetectTones
title: ITLegacyCallMediaControl2::DetectTones (tapi3if.h)
description: The DetectTones method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
helpviewer_keywords: ["DetectTones","DetectTones method [TAPI 2.2]","DetectTones method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","DetectTones method","ITLegacyCallMediaControl2.DetectTones","ITLegacyCallMediaControl2::DetectTones","_tapi3_itlegacycallmediacontrol2_detecttones","tapi3.itlegacycallmediacontrol2_detecttones","tapi3if/ITLegacyCallMediaControl2::DetectTones"]
old-location: tapi3\itlegacycallmediacontrol2_detecttones.htm
tech.root: tapi3
ms.assetid: e059bfc0-3701-4e07-8c30-0a2512731080
ms.date: 12/05/2018
ms.keywords: DetectTones, DetectTones method [TAPI 2.2], DetectTones method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],DetectTones method, ITLegacyCallMediaControl2.DetectTones, ITLegacyCallMediaControl2::DetectTones, _tapi3_itlegacycallmediacontrol2_detecttones, tapi3.itlegacycallmediacontrol2_detecttones, tapi3if/ITLegacyCallMediaControl2::DetectTones
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
 - ITLegacyCallMediaControl2::DetectTones
 - tapi3if/ITLegacyCallMediaControl2::DetectTones
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
 - ITLegacyCallMediaControl2.DetectTones
---

# ITLegacyCallMediaControl2::DetectTones


## -description

The 
<b>DetectTones</b> method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.

This method is intended for C/C++ applications. Visual Basic and scripting applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a> method instead.

## -parameters

### -param pToneList [in]

Pointer to a 
<a href="/windows/desktop/api/tapi3if/ns-tapi3if-tapi_detecttone">TAPI_DETECTTONE</a> array that specifies the tones to detect. Each tone in the array has an application-defined tag field that is used to identify the individual tones in the list when a tone detection event of type <b>TE_TONEEVENT</b> is reported. For more information, see the following Remarks section.

### -param lNumTones [in]

The number of entries in the array specified by the <i>pToneList</i> parameter. This parameter is ignored if <i>pToneList</i> is <b>NULL</b>.

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
The <i>pToneList</i> parameter is not a valid pointer.

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
<b>DetectTones</b> method and specify a <b>NULL</b><i>pToneList</i> parameter. To change the list of tones to monitor, call this method and specify a new tone list.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>



<a href="/windows/desktop/api/tapi3if/ns-tapi3if-tapi_detecttone">TAPI_DETECTTONE</a>