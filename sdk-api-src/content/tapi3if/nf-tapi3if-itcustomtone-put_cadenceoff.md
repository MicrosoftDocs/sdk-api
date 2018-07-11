---
UID: NF:tapi3if.ITCustomTone.put_CadenceOff
title: ITCustomTone::put_CadenceOff
author: windows-sdk-content
description: The put_CadenceOff method sets the &#0034;off&#0034; duration of the cadence of the custom tone to generate.
old-location: tapi3\itcustomtone_put_cadenceoff.htm
old-project: tapi
ms.assetid: 056e1ca5-2bce-4a69-9b30-2ac142bcb52b
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],put_CadenceOff method, ITCustomTone.put_CadenceOff, ITCustomTone::put_CadenceOff, _tapi3_itcustomtone_put_cadenceoff, put_CadenceOff, put_CadenceOff method [TAPI 2.2], put_CadenceOff method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_put_cadenceoff, tapi3if/ITCustomTone::put_CadenceOff
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCustomTone.put_CadenceOff
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCustomTone::put_CadenceOff


## -description


The 
<b>put_CadenceOff</b> method sets the "off" duration of the cadence of the custom tone to generate.


## -parameters




### -param lCadenceOff [in]

Specifies the "off" duration, in milliseconds, of the cadence of the custom tone to generate. Zero means no off time, that is, a constant tone.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/0d561ab6-fc38-4058-9443-d7825eae2dc5">get_CadenceOff</a>
 

 

