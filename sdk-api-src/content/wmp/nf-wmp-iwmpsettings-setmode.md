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

# IWMPSettings::setMode


## -description



The <b>setMode</b> method sets the state of playback options.




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
<td>Tracks are restarted at the beginning after playing to the end. Default state is true.</td>
</tr>
<tr>
<td>loop</td>
<td>The sequence of tracks repeats itself. Default state is false.</td>
</tr>
<tr>
<td>showFrame</td>
<td>The nearest video keyframe is displayed when not playing. Default state is false. Has no effect on audio tracks.</td>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order. Default state is false.</td>
</tr>
</table>
 


### -param varfMode [in]

<b>VARIANT_BOOL</b> specifying whether the specified mode is active.


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
 




## -remarks



When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame. Use this mode cautiously when playing non-local content.




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/5275cb99-8007-4af2-9137-694de18c5434">IWMPSettings::getMode</a>
 

 

