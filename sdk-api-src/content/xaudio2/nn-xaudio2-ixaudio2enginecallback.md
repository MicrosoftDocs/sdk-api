---
UID: NN:xaudio2.IXAudio2EngineCallback
title: IXAudio2EngineCallback
author: windows-sdk-content
description: The IXAudio2EngineCallback interface contains methods that notify the client when certain events happen in the IXAudio2 engine.
old-location: xaudio2\ixaudio2enginecallback.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2enginecallback.IXAudio2EngineCallback
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXAudio2EngineCallback, IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs], IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2enginecallback, xaudio2/IXAudio2EngineCallback
ms.topic: interface
req.header: xaudio2.h
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2EngineCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2EngineCallback interface


## -description


The IXAudio2EngineCallback interface contains methods that notify the client when certain events happen in the <a href="https://msdn.microsoft.com/en-us/library/Ee415908(v=VS.85).aspx">IXAudio2</a> engine.

This interface should be implemented by the XAudio2 client. XAudio2 calls these methods via an interface pointer provided by the client, using the <a href="https://msdn.microsoft.com/en-us/library/Ee419212(v=VS.85).aspx">XAudio2Create</a> method. Methods in this interface return <b>void</b>, rather than an HRESULT. 


See <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> for restrictions on callback implementation.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>IXAudio2EngineCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418461(v=VS.85).aspx">OnCriticalError</a>
</td>
<td align="left" width="63%">
Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418462(v=VS.85).aspx">OnProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just after an audio processing pass ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418463(v=VS.85).aspx">OnProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just before an audio processing pass begins.

</td>
</tr>
</table> 


## -members

The <b>IXAudio2EngineCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418461(v=VS.85).aspx">OnCriticalError</a>
</td>
<td align="left" width="63%">
Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418462(v=VS.85).aspx">OnProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just after an audio processing pass ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee418463(v=VS.85).aspx">OnProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called by XAudio2 just before an audio processing pass begins.

</td>
</tr>
</table>Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.

Called by XAudio2 just after an audio processing pass ends.

Called by XAudio2 just before an audio processing pass begins.

 

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>



<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 

