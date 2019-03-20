---
UID: NF:tapi3if.ITCustomTone.put_CadenceOn
title: ITCustomTone::put_CadenceOn (tapi3if.h)
author: windows-sdk-content
description: The put_CadenceOn method sets the &#0034;on&#0034; duration of the cadence of the custom tone to generate.
old-location: tapi3\itcustomtone_put_cadenceon.htm
tech.root: Tapi
ms.assetid: c4403c3a-7dd8-4707-ac23-5a478fffce17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],put_CadenceOn method, ITCustomTone.put_CadenceOn, ITCustomTone::put_CadenceOn, _tapi3_itcustomtone_put_cadenceon, put_CadenceOn, put_CadenceOn method [TAPI 2.2], put_CadenceOn method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_put_cadenceon, tapi3if/ITCustomTone::put_CadenceOn
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
 - ITCustomTone.put_CadenceOn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCustomTone::put_CadenceOn


## -description


The 
<b>put_CadenceOn</b> method sets the "on" duration of the cadence of the custom tone to generate.


## -parameters




### -param CadenceOn [in]

Specifies the "on" duration, in milliseconds, of the cadence of the custom tone to generate. Zero means no tone is generated.


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



<a href="https://msdn.microsoft.com/2f3da359-69e1-40a3-bfd6-42ade8de2379">get_CadenceOn</a>
 

 

