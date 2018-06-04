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

# IDirectMusicSynth interface


## -description


The <code>IDirectMusicSynth</code> interface is used by DirectMusic to communicate with user-mode synthesizers. If you create a custom software synthesizer that runs in user mode, it should have an <code>IDirectMusicSynth</code> interface to plug into DirectMusic. <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface.

The synthesizer is not complete without a connection to a wave sink, which is represented as an object with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536520">IDirectMusicSynthSink</a> interface. For more information, see <a href="https://msdn.microsoft.com/ce9a353b-9e4b-402b-92bb-948200e3c2ef">IDirectMusicSynth and IDirectMusicSynthSink</a>.

In addition to the methods that <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface, <code>IDirectMusicSynth</code> supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536529">IDirectMusicSynth::Activate</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536531">IDirectMusicSynth::Close</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536532">IDirectMusicSynth::Download</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536533">IDirectMusicSynth::GetAppend</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536534">IDirectMusicSynth::GetChannelPriority</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536535">IDirectMusicSynth::GetFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536536">IDirectMusicSynth::GetLatencyClock</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536537">IDirectMusicSynth::GetPortCaps</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536538">IDirectMusicSynth::GetRunningStats</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536539">IDirectMusicSynth::Open</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536540">IDirectMusicSynth::PlayBuffer</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536541">IDirectMusicSynth::Render</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536542">IDirectMusicSynth::SetChannelPriority</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536543">IDirectMusicSynth::SetMasterClock</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536544">IDirectMusicSynth::SetNumChannelGroups</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536545">IDirectMusicSynth::SetSynthSink</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536546">IDirectMusicSynth::Unload</a>


</dd>
</dl>
