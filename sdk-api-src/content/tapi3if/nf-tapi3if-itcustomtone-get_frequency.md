---
UID: NF:tapi3if.ITCustomTone.get_Frequency
title: ITCustomTone::get_Frequency
author: windows-sdk-content
description: The get_Frequency method retrieves the frequency of the tone component to generate.
old-location: tapi3\itcustomtone_get_frequency.htm
tech.root: Tapi
ms.assetid: 2521d754-234a-4ef0-a3b2-23cea999ad45
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],get_Frequency method, ITCustomTone.get_Frequency, ITCustomTone::get_Frequency, _tapi3_itcustomtone_get_frequency, get_Frequency, get_Frequency method [TAPI 2.2], get_Frequency method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_get_frequency, tapi3if/ITCustomTone::get_Frequency
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
 - ITCustomTone.get_Frequency
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
- ITCustomTone.get_Frequency
: 
---

# ITCustomTone::get_Frequency


## -description


The 
<b>get_Frequency</b> method retrieves the frequency of the tone component to generate.


## -parameters




### -param plFrequency [out]

Pointer to a value to receive the frequency, in hertz, of the tone component.


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
The <i>plFrequency</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/1faae20a-40a7-48d7-9621-5f1761c28773">put_Frequency</a>
 

 

