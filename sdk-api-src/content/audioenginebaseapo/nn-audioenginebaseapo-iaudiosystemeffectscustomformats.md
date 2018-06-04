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

# IAudioSystemEffectsCustomFormats interface


## -description


The <code>IAudioSystemEffectsCustomFormats</code> interface is supported in Windows Vista and later versions of Windows. When you develop an audio processing object (APO) to drive an audio adapter with  an atypical format, the APO must support the <code>IAudioSystemEffectsCustomFormats</code> interface.

The Windows operating system can instantiate your APO outside the audio engine and use the <code>IAudioSystemEffectsCustomFormats</code> interface to retrieve information about the atypical format. The associated user interface displays the data that is retrieved.
<div class="alert"><b>Important</b>  Although the <code>IAudioSystemEffectsCustomFormats</code> interface  continues to be supported in Windows, note that the type of APO to which you can apply this interface depends on the version of Windows you are targeting. The following table provides more information:</div><div> </div><table>
<tr>
<th>Target OS</th>
<th>Target APO type</th>
</tr>
<tr>
<td>Windows Vista</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 7</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 8</td>
<td>Global effects (GFX)</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>Endpoint effects (EFX)</td>
</tr>
</table> 

The <code>IAudioSystemEffectsCustomFormats</code> interface inherits from <b>IUnknown</b> and also supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536516">IAudioSystemEffectsCustomFormats::GetFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536517">IAudioSystemEffectsCustomFormats::GetFormatCount</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536518">IAudioSystemEffectsCustomFormats::GetFormatRepresentation</a>


</dd>
</dl>
