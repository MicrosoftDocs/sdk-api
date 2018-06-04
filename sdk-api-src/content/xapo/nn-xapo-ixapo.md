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

# IXAPO interface


## -description


The interface for an Audio Processing Object which be used in an XAudio2 effect chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAPO</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXAPO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAPO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2F7D490-1306-46A0-9547-30F7AB16825C">CalcInputFrames</a>
</td>
<td align="left" width="63%">
Returns the number of input frames required to generate the given number of output frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A7DD6AD8-6EF4-46D2-B7B1-3D70A9408E78">CalcOutputFrames</a>
</td>
<td align="left" width="63%">
Returns the number of output frames that will be generated from a given number of input frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn425142">GetRegistrationProperties</a>
</td>
<td align="left" width="63%">
Returns the registration properties of an XAPO. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Performs any effect-specific initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3CD26BF0-9EA5-434F-9B97-D375FB6B7D21">IsInputFormatSupported</a>
</td>
<td align="left" width="63%">
Queries if a specific input format is supported for a given output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5921C1C2-91DF-4E1F-A179-786CEB997BAF">IsOutputFormatSupported</a>
</td>
<td align="left" width="63%">
Queries if a specific output format is supported for a given input format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">LockForProcess</a>
</td>
<td align="left" width="63%">
Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a> is called on the realtime thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a>
</td>
<td align="left" width="63%">
Runs the XAPO's digital signal processing (DSP) code on the given input and output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets variables dependent on frame history.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1D70B361-6EB6-4591-9AD2-2E802F6EE341">UnlockForProcess</a>
</td>
<td align="left" width="63%">
Deallocates variables that were allocated with the <a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">LockForProcess</a> method.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

