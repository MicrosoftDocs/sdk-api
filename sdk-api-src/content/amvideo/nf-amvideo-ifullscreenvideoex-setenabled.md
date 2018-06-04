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

# IFullScreenVideoEx::SetEnabled


## -description



The <code>SetEnabled</code> method enables or disables a specified display mode.




## -parameters




### -param Mode [in]

Index of the display mode to enable or disable.


### -param bEnabled [in]

Specifies one of the following Boolean values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OATRUE"></a><a id="oatrue"></a><dl>
<dt><b>OATRUE</b></dt>
</dl>
</td>
<td width="60%">
Enable the specified display mode.

</td>
</tr>
<tr>
<td width="40%"><a id="OAFALSE"></a><a id="oafalse"></a><dl>
<dt><b>OAFALSE</b></dt>
</dl>
</td>
<td width="60%">
Disable the specified display mode.

</td>
</tr>
</table>
 


## -returns



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
<td>E_INVALIDARG</td>
<td>Invalid argument.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
</table>
 




## -remarks



The Full Screen Renderer supports a static set of display modes. By default, every mode is enabled. You can use this method to enable or disable a particular display mode. The video card on the user's system might not support every mode. The Full Screen Renderer will not use a mode that the video card does not support, even if that mode is enabled. To determine whether the card supports a particular mode, call the <a href="https://msdn.microsoft.com/9b05d6c6-522c-46b8-90b5-c4650cee5f6b">IFullScreenVideoEx::IsModeAvailable</a> method. If a mode is disabled, the Full Screen Renderer will not use it, even if the card supports it.

Display modes are indexed from zero. The <a href="https://msdn.microsoft.com/70d4e124-083b-4729-8f39-778e815ea23b">IFullScreenVideoEx::CountModes</a> method returns the number of modes. To retrieve the width, height, and bit depth of a particular display mode, call the <a href="https://msdn.microsoft.com/c1a4aea8-8c48-4073-80ed-060db5adb514">IFullScreenVideoEx::GetModeInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

