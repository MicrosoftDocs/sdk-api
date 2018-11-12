---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateCustomTones
title: ITLegacyCallMediaControl2::GenerateCustomTones
author: windows-sdk-content
description: The GenerateCustomTones method generates the specified custom tone.
old-location: tapi3\itlegacycallmediacontrol2_generatecustomtones.htm
tech.root: tapi
ms.assetid: fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GenerateCustomTones, GenerateCustomTones method [TAPI 2.2], GenerateCustomTones method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateCustomTones method, ITLegacyCallMediaControl2.GenerateCustomTones, ITLegacyCallMediaControl2::GenerateCustomTones, _tapi3_itlegacycallmediacontrol2_generatecustomtones, tapi3.itlegacycallmediacontrol2_generatecustomtones, tapi3if/ITLegacyCallMediaControl2::GenerateCustomTones
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyCallMediaControl2.GenerateCustomTones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::GenerateCustomTones


## -description


The 
<b>GenerateCustomTones</b> method generates the specified custom tone.

This method is intended for C/C++ applications. Visual Basic and scripting applications should use the 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a> method instead.


## -parameters




### -param pToneList [in]

Pointer to a 
<a href="https://msdn.microsoft.com/1d3c7b25-92a8-41f5-8186-f6425cc6be74">TAPI_CUSTOMTONE</a> array that specifies the tones to generate.


### -param lNumTones [in]

The number of entries in the array specified by the <i>pToneList</i> parameter.


### -param lDuration [in]

The duration, in milliseconds, during which the tone should be sustained.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method translates to a call to the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/d5975bd0-2406-45a8-9631-80f40a860204">lineGenerateTone</a> function.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>



<a href="https://msdn.microsoft.com/1d3c7b25-92a8-41f5-8186-f6425cc6be74">TAPI_CUSTOMTONE</a>
 

 

