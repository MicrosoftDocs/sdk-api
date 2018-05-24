---
UID: NN:imapi2.IDiscFormat2TrackAtOnce
title: IDiscFormat2TrackAtOnce
author: windows-driver-content
description: Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.
old-location: imapi\idiscformat2trackatonce.htm
old-project: imapi
ms.assetid: 27f2d248-1c83-4784-82f9-75ce0a038b87
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IDiscFormat2TrackAtOnce, IDiscFormat2TrackAtOnce interface [IMAPI], IDiscFormat2TrackAtOnce interface [IMAPI],described, imapi.idiscformat2trackatonce, imapi2/IDiscFormat2TrackAtOnce
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2TrackAtOnce
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2TrackAtOnce interface


## -description


Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2TrackAtOnce) for the class identifier and __uuidof(IDiscFormat2TrackAtOnce) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2TrackAtOnce</b> interface inherits from <a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>. <b>IDiscFormat2TrackAtOnce</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2TrackAtOnce</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ac74b91-b0c7-471f-b6a9-1393d677e0c1">AddAudioTrack</a>
</td>
<td align="left" width="63%">
Writes the data stream to the current media as a new track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09e71d36-da1d-4ba0-bd6b-4ce4425d481a">CancelAddTrack</a>
</td>
<td align="left" width="63%">
Cancels adding the new track to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8223c46b-b754-47a1-aab9-0ebb949e79f8">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c259233b-4e36-4ee2-8068-d77ece1e927e">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c921a12-9e9d-48af-af3d-0f62aff49e65">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a80eee3-6b85-432a-878c-c8e4cade7be1">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8236dc3f-fe94-4dd5-908b-36ed74943ad4">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f33bbc2-531a-472a-8e2a-b7e9fb4d6bba">get_DoNotFinalizeMedia</a>
</td>
<td align="left" width="63%">
Determines if the media is left open for writing after writing the audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b414bdbc-0f49-4a00-9b25-fa738f5f880b">get_ExpectedTableOfContents</a>
</td>
<td align="left" width="63%">
Retrieves the table of content for the audio tracks that were laid on the media within the track-writing session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a36dd3de-ca08-4783-beca-95813402692b">get_FreeSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of sectors available for adding a new track to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a8bcfe2-d09a-4eec-8e68-5e0dfc868033">get_NumberOfExistingTracks</a>
</td>
<td align="left" width="63%">
Retrieves the number of existing audio tracks on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62a60ffb-4a9b-4921-b7fa-acc5a439e92b">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3702f4c1-4043-4a69-bd6b-4346c560651a">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fe83f25-9d7d-472d-9b84-90e00c0b5a51">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0aefc38-c679-4492-becc-a8c8563ea948">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b95b7fb9-6e4b-4d9d-86fe-64ca92343225">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86af52be-d1ea-4ccb-b1b4-e301d70cac53">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total sectors available on the media if writing one continuous audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85bbb2a8-6ff9-4af4-aefd-fca85f727f37">get_UsedSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total number of used sectors on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">PrepareMedia</a>
</td>
<td align="left" width="63%">
Locks the current media for exclusive access. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a19bd7-9302-49f5-a5e5-573bf72725a3">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9140aa9f-f592-4ef4-85c7-321e5503b0b8">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffde10f9-259a-400d-b83e-f8c81bbe8f94">put_DoNotFinalizeMedia</a>
</td>
<td align="left" width="63%">
Determines if the media is left open for writing after writing the audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d67b076-0c3f-4d1f-aa19-8e22dd98f331">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d6f85a9-94cc-426c-8442-14eb6e4024f3">ReleaseMedia</a>
</td>
<td align="left" width="63%">
Closes the track-writing session and releases the lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29c4487a-4247-45cf-af95-dc85fafb05c5">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscFormat2TrackAtOnce</b> object in a script, use IMAPI2.MsftDiscFormat2TrackAtOnce as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://msdn.microsoft.com/5223c9f6-30f6-43ce-b46c-267da0a53d4b">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>



<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>
 

 

