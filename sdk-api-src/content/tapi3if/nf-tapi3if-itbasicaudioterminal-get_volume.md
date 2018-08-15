---
UID: NF:tapi3if.ITBasicAudioTerminal.get_Volume
title: ITBasicAudioTerminal::get_Volume
author: windows-sdk-content
description: The get_Volume method gets the volume.
old-location: tapi3\itbasicaudioterminal_get_volume.htm
old-project: tapi
ms.assetid: 2d3a64fa-41b6-44c4-a67e-08113e771cc7
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITBasicAudioTerminal interface [TAPI 2.2],get_Volume method, ITBasicAudioTerminal.get_Volume, ITBasicAudioTerminal::get_Volume, _tapi3_itbasicaudioterminal_get_volume, get_Volume, get_Volume method [TAPI 2.2], get_Volume method [TAPI 2.2],ITBasicAudioTerminal interface, tapi3.itbasicaudioterminal_get_volume, tapi3if/ITBasicAudioTerminal::get_Volume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITBasicAudioTerminal.get_Volume
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicAudioTerminal::get_Volume


## -description


The 
<b>get_Volume</b> method gets the volume.


## -parameters




### -param plVolume [out]

Pointer to volume. The volume property is a value between 0 and FFFF, representing a set of logarithmic steps. Not all devices support as many distinguishable steps.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

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




<a href="https://msdn.microsoft.com/3e676a16-f3ce-433c-9941-8cdccdb01efd">ITBasicAudioTerminal</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/6c611505-74b4-48fa-bb36-ec765cb24f96">put_Volume</a>
 

 

