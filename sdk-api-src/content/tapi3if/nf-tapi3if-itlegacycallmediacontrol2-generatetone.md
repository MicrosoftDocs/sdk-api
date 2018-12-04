---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GenerateTone
title: ITLegacyCallMediaControl2::GenerateTone
author: windows-sdk-content
description: The GenerateTone method generates the specified tone.
old-location: tapi3\itlegacycallmediacontrol2_generatetone.htm
tech.root: tapi
ms.assetid: 4c77ee53-3c40-4fdc-9a35-40a8e74b4ec4
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: GenerateTone, GenerateTone method [TAPI 2.2], GenerateTone method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GenerateTone method, ITLegacyCallMediaControl2.GenerateTone, ITLegacyCallMediaControl2::GenerateTone, _tapi3_itlegacycallmediacontrol2_generatetone, tapi3.itlegacycallmediacontrol2_generatetone, tapi3if/ITLegacyCallMediaControl2::GenerateTone
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
 - ITLegacyCallMediaControl2.GenerateTone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::GenerateTone


## -description


The 
<b>GenerateTone</b> method generates the specified tone.

To generate custom tones, call the 
<a href="https://msdn.microsoft.com/fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4">GenerateCustomTones</a> (C/C++) or the 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a> method (Visual Basic and scripting applications).


## -parameters




### -param ToneMode [in]

Indicates the tone mode. The values used are those from the 
<a href="https://msdn.microsoft.com/eeae9d4a-824c-4316-8eb3-846563ac4a54">TAPI_TONEMODE</a> enumeration.


### -param lDuration [in]

Both the duration, in milliseconds, of DTMF digits and pulse, and DTMF interdigit spacing.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

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



This method translates to a call to the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/d5975bd0-2406-45a8-9631-80f40a860204">lineGenerateTone</a> function.

When tone generation finishes, an event of type TE_GENERATEEVENT is generated.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

