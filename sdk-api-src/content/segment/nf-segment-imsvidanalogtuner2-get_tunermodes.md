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

# IMSVidAnalogTuner2::get_TunerModes


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_TunerModes</b> method retrieves a flag value that indicates which modes the tuner supports, such as TV or FM.


## -parameters




### -param Modes [out]

Pointer to a variable that receives the modes flag. Possible values are the sum of one or more of the values in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0x0000</td>
<td>Default tuner mode.</td>
</tr>
<tr>
<td>0x0001</td>
<td>TV tuner mode.</td>
</tr>
<tr>
<td>0x0002</td>
<td>FM radio tuner mode.</td>
</tr>
<tr>
<td>0x0004</td>
<td>AM radio tuner mode.</td>
</tr>
</table>
 




## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/50d30a45-8cea-454c-b5d2-ff809b8a8206">IMSVidAnalogTuner2 Interface</a>
 

 

