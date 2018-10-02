---
UID: NN:dmusics.IDirectMusicSynth
title: IDirectMusicSynth
author: windows-sdk-content
description: The IDirectMusicSynth interface is used by DirectMusic to communicate with user-mode synthesizers.
old-location: audio\idirectmusicsynth.htm
tech.root: audio
ms.assetid: 08f1056a-fead-475b-a13a-ee11b9709241
ms.author: windowssdkdev
ms.date: 09/28/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectMusicSynth interface


## -description


The <code>IDirectMusicSynth</code> interface is used by DirectMusic to communicate with user-mode synthesizers. If you create a custom software synthesizer that runs in user mode, it should have an <code>IDirectMusicSynth</code> interface to plug into DirectMusic. <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface.

The synthesizer is not complete without a connection to a wave sink, which is represented as an object with an <a href="https://msdn.microsoft.com/11944933-cd95-4979-82b2-2c3875b221b3">IDirectMusicSynthSink</a> interface. For more information, see <a href="https://msdn.microsoft.com/ce9a353b-9e4b-402b-92bb-948200e3c2ef">IDirectMusicSynth and IDirectMusicSynthSink</a>.

In addition to the methods that <code>IDirectMusicSynth</code> inherits from the <b>IUnknown</b> interface, <code>IDirectMusicSynth</code> supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/9efdb079-ed24-43b4-844b-344571399de7">IDirectMusicSynth::Activate</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/275d9ad3-9dde-4cfb-a67f-24da3a0ad2ce">IDirectMusicSynth::Close</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/2f36654c-25bf-47c3-a4d6-990d427bd1fc">IDirectMusicSynth::Download</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/fc250e51-2e7d-4406-a8cf-7b7430a0ef7c">IDirectMusicSynth::GetAppend</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/be49f7eb-f0ab-48b3-9776-79811309fcee">IDirectMusicSynth::GetChannelPriority</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/4fa55ff5-4f72-4f8b-bf11-64f07b054ff5">IDirectMusicSynth::GetFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/36690d54-dc88-4e31-8f66-8a0b48be2712">IDirectMusicSynth::GetLatencyClock</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/9e4ba4e3-5bd7-4a90-a591-8bffaa0265d0">IDirectMusicSynth::GetPortCaps</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/cf3e97f2-6068-4438-b4c7-5e55ba22bd6e">IDirectMusicSynth::GetRunningStats</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/15a16b27-7693-4fc6-80ae-e8aedcf879d0">IDirectMusicSynth::Open</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/96d0a2ef-1265-4e04-bb70-920f4c82058c">IDirectMusicSynth::PlayBuffer</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/c0aea93c-df92-46e6-9cd7-38235f513924">IDirectMusicSynth::Render</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/6398f460-4c2e-4995-a606-e95e0488f1cd">IDirectMusicSynth::SetChannelPriority</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/1585cfcc-2c83-4705-b465-52a621ccc163">IDirectMusicSynth::SetMasterClock</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/b7a26fc6-11a9-4bb6-944f-dfbc772b4383">IDirectMusicSynth::SetNumChannelGroups</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/51153ea3-7c61-458a-8879-10efbd678b53">IDirectMusicSynth::SetSynthSink</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/608ebffe-873a-40ed-a411-245e8b6ceabd">IDirectMusicSynth::Unload</a>


</dd>
</dl>
