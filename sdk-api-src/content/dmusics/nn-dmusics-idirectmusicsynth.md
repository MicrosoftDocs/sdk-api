---
UID: NN:dmusics.IDirectMusicSynth
title: IDirectMusicSynth
author: windows-sdk-content
description: The IDirectMusicSynth interface is used by DirectMusic to communicate with user-mode synthesizers.
old-location: audio\idirectmusicsynth.htm
old-project: audio
ms.assetid: 08f1056a-fead-475b-a13a-ee11b9709241
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IDirectMusicSynth, IDirectMusicSynth interface [Audio Devices], IDirectMusicSynth interface [Audio Devices],described, audio.idirectmusicsynth, audmp-routines_ab253bc7-f9a6-4279-99fb-4e5b2693c94b.xml, dmusics/IDirectMusicSynth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dmusics.h
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
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dmusics.h
api_name:
-	IDirectMusicSynth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
