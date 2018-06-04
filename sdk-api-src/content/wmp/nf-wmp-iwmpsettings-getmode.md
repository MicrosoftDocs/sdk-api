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

# IWMPSettings::getMode


## -description



The <b>getMode</b> method determines whether the loop mode or shuffle mode is active.




## -parameters




### -param bstrMode [in]

<b>BSTR</b> containing one of the following values.

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
<td>autoRewind</td>
<td>Tracks are restarted from the beginning after playing to the end.</td>
</tr>
<tr>
<td>loop</td>
<td>The sequence of tracks repeats itself.</td>
</tr>
<tr>
<td>showFrame</td>
<td>The nearest key frame is displayed when not playing. This mode is not relevant for audio tracks.</td>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order.</td>
</tr>
</table>
 


### -param pvarfMode [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the specified mode is active.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/28a404a7-5bb0-41bb-a5b2-cc6138b8176e">IWMPSettings::setMode</a>
 

 

