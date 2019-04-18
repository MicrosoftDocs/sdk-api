---
UID: NF:tapi3if.ITCustomTone.get_Volume
title: ITCustomTone::get_Volume (tapi3if.h)
author: windows-sdk-content
description: The get_Volume method retrieves the volume level at which to generate the tone.
old-location: tapi3\itcustomtone_get_volume.htm
tech.root: Tapi
ms.assetid: 28eead55-915a-4bb6-9915-ebd56c9d123d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],get_Volume method, ITCustomTone.get_Volume, ITCustomTone::get_Volume, _tapi3_itcustomtone_get_volume, get_Volume, get_Volume method [TAPI 2.2], get_Volume method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_get_volume, tapi3if/ITCustomTone::get_Volume
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
 - ITCustomTone.get_Volume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCustomTone::get_Volume


## -description


The 
<b>get_Volume</b> method retrieves the volume level at which to generate the tone.


## -parameters




### -param plVolume [out]

Pointer to a value to receive the volume level. A value of 0x0000FFFF represents full volume; a value of 0x00000000 represents silence.


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
The <i>plVolume</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2c51048-93aa-4469-b00e-911e62b5702d">ITCustomTone</a>



<a href="https://msdn.microsoft.com/2de6dbc3-9a3d-48e7-b9e1-56b3e25d1b60">put_Volume</a>
 

 

