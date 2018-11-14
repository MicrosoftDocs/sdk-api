---
UID: NF:tapi3if.ITLegacyCallMediaControl2.DetectTones
title: ITLegacyCallMediaControl2::DetectTones
author: windows-sdk-content
description: The DetectTones method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
old-location: tapi3\itlegacycallmediacontrol2_detecttones.htm
tech.root: tapi
ms.assetid: e059bfc0-3701-4e07-8c30-0a2512731080
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DetectTones, DetectTones method [TAPI 2.2], DetectTones method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],DetectTones method, ITLegacyCallMediaControl2.DetectTones, ITLegacyCallMediaControl2::DetectTones, _tapi3_itlegacycallmediacontrol2_detecttones, tapi3.itlegacycallmediacontrol2_detecttones, tapi3if/ITLegacyCallMediaControl2::DetectTones
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
 - ITLegacyCallMediaControl2.DetectTones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITLegacyCallMediaControl2.DetectTones
: 
---

# ITLegacyCallMediaControl2::DetectTones


## -description


The 
<b>DetectTones</b> method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.

This method is intended for C/C++ applications. Visual Basic and scripting applications should use the 
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a> method instead.


## -parameters




### -param pToneList [in]

Pointer to a 
<a href="https://msdn.microsoft.com/c0e311e8-67b5-4dae-848e-589f306191fa">TAPI_DETECTTONE</a> array that specifies the tones to detect. Each tone in the array has an application-defined tag field that is used to identify the individual tones in the list when a tone detection event of type <b>TE_TONEEVENT</b> is reported. For more information, see the following Remarks section.


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
<a href="https://msdn.microsoft.com/47fe21f2-7896-4ccf-8c26-33430b2081ac">lineMonitorTones</a> call.

To cancel tone monitoring in progress, call the 
<b>DetectTones</b> method and specify a <b>NULL</b><i>pToneList</i> parameter. To change the list of tones to monitor, call this method and specify a new tone list.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>



<a href="https://msdn.microsoft.com/c0e311e8-67b5-4dae-848e-589f306191fa">TAPI_DETECTTONE</a>
 

 

