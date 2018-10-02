---
UID: NF:tapi3if.ITCustomTone.get_CadenceOff
title: ITCustomTone::get_CadenceOff
author: windows-sdk-content
description: The get_CadenceOff method retrieves the &#0034;off&#0034; duration of the cadence of the custom tone to generate.
old-location: tapi3\itcustomtone_get_cadenceoff.htm
tech.root: TAPI
ms.assetid: 0d561ab6-fc38-4058-9443-d7825eae2dc5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],get_CadenceOff method, ITCustomTone.get_CadenceOff, ITCustomTone::get_CadenceOff, _tapi3_itcustomtone_get_cadenceoff, get_CadenceOff, get_CadenceOff method [TAPI 2.2], get_CadenceOff method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_get_cadenceoff, tapi3if/ITCustomTone::get_CadenceOff
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
 - ITCustomTone.get_CadenceOff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCustomTone::get_CadenceOff


## -description


The 
<b>get_CadenceOff</b> method retrieves the "off" duration of the cadence of the custom tone to generate.


## -parameters




### -param plCadenceOff [out]

Pointer to a value to receive the "off" duration, in milliseconds, of the cadence of the custom tone. Zero means no off time, that is, a constant tone.


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
The <i>plCadenceOff</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/056e1ca5-2bce-4a69-9b30-2ac142bcb52b">put_CadenceOff</a>
 

 

