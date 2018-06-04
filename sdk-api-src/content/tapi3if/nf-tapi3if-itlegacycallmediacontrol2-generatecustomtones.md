---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

