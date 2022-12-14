---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateCustomTones
title: ITLegacyCallMediaControl2::GenerateCustomTones (tapi3if.h)
description: The GenerateCustomTones method generates the specified custom tone.
helpviewer_keywords: ["GenerateCustomTones","GenerateCustomTones method [TAPI 2.2]","GenerateCustomTones method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","GenerateCustomTones method","ITLegacyCallMediaControl2.GenerateCustomTones","ITLegacyCallMediaControl2::GenerateCustomTones","_tapi3_itlegacycallmediacontrol2_generatecustomtones","tapi3.itlegacycallmediacontrol2_generatecustomtones","tapi3if/ITLegacyCallMediaControl2::GenerateCustomTones"]
old-location: tapi3\itlegacycallmediacontrol2_generatecustomtones.htm
tech.root: tapi3
ms.assetid: fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4
ms.date: 12/05/2018
ms.keywords: GenerateCustomTones, GenerateCustomTones method [TAPI 2.2], GenerateCustomTones method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateCustomTones method, ITLegacyCallMediaControl2.GenerateCustomTones, ITLegacyCallMediaControl2::GenerateCustomTones, _tapi3_itlegacycallmediacontrol2_generatecustomtones, tapi3.itlegacycallmediacontrol2_generatecustomtones, tapi3if/ITLegacyCallMediaControl2::GenerateCustomTones
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
 - ITLegacyCallMediaControl2::GenerateCustomTones
 - tapi3if/ITLegacyCallMediaControl2::GenerateCustomTones
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
 - ITLegacyCallMediaControl2.GenerateCustomTones
---

# ITLegacyCallMediaControl2::GenerateCustomTones


## -description

The 
<b>GenerateCustomTones</b> method generates the specified custom tone.

This method is intended for C/C++ applications. Visual Basic and scripting applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">GenerateCustomTonesByCollection</a> method instead.

## -parameters

### -param pToneList [in]

Pointer to a 
<a href="/windows/desktop/api/tapi3if/ns-tapi3if-tapi_customtone">TAPI_CUSTOMTONE</a> array that specifies the tones to generate.

### -param lNumTones [in]

The number of entries in the array specified by the <i>pToneList</i> parameter.

### -param lDuration [in]

The duration, in milliseconds, during which the tone should be sustained.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method translates to a call to the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratetone">lineGenerateTone</a> function.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>



<a href="/windows/desktop/api/tapi3if/ns-tapi3if-tapi_customtone">TAPI_CUSTOMTONE</a>