---
UID: NF:tapi3if.ITCustomTone.get_CadenceOn
title: ITCustomTone::get_CadenceOn
author: windows-sdk-content
description: The get_CadenceOn method retrieves the &#0034;on&#0034; duration of the cadence of the custom tone to generate.
old-location: tapi3\itcustomtone_get_cadenceon.htm
tech.root: tapi
ms.assetid: 2f3da359-69e1-40a3-bfd6-42ade8de2379
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],get_CadenceOn method, ITCustomTone.get_CadenceOn, ITCustomTone::get_CadenceOn, _tapi3_itcustomtone_get_cadenceon, get_CadenceOn, get_CadenceOn method [TAPI 2.2], get_CadenceOn method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_get_cadenceon, tapi3if/ITCustomTone::get_CadenceOn
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
 - ITCustomTone.get_CadenceOn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCustomTone::get_CadenceOn


## -description


The 
<b>get_CadenceOn</b> method retrieves the "on" duration of the cadence of the custom tone to generate.


## -parameters




### -param plCadenceOn [out]

Pointer to a value to receive the "on" duration, in milliseconds, of the cadence of the custom tone. Zero means no tone is generated.


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
The <i>plCadenceOn</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/c4403c3a-7dd8-4707-ac23-5a478fffce17">put_CadenceOn</a>
 

 

