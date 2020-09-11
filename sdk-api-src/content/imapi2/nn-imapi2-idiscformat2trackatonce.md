---
UID: NN:imapi2.IDiscFormat2TrackAtOnce
title: IDiscFormat2TrackAtOnce (imapi2.h)
description: Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.
helpviewer_keywords: ["IDiscFormat2TrackAtOnce","IDiscFormat2TrackAtOnce interface [IMAPI]","IDiscFormat2TrackAtOnce interface [IMAPI]","described","imapi.idiscformat2trackatonce","imapi2/IDiscFormat2TrackAtOnce"]
old-location: imapi\idiscformat2trackatonce.htm
tech.root: imapi
ms.assetid: 27f2d248-1c83-4784-82f9-75ce0a038b87
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce, IDiscFormat2TrackAtOnce interface [IMAPI], IDiscFormat2TrackAtOnce interface [IMAPI],described, imapi.idiscformat2trackatonce, imapi2/IDiscFormat2TrackAtOnce
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscFormat2TrackAtOnce
 - imapi2/IDiscFormat2TrackAtOnce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2TrackAtOnce
---

# IDiscFormat2TrackAtOnce interface


## -description

Use this interface to write audio to blank CD-R or CD-RW media in Track-At-Once mode.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2TrackAtOnce) for the class identifier and __uuidof(IDiscFormat2TrackAtOnce) for the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2TrackAtOnce</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2TrackAtOnce</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-addaudiotrack">AddAudioTrack</a>
</td>
<td align="left" width="63%">
Writes the data stream to the current media as a new track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-canceladdtrack">CancelAddTrack</a>
</td>
<td align="left" width="63%">
Cancels adding the new track to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_bufferunderrunfreedisabled">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_clientname">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_currentphysicalmediatype">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_currentrotationtypeispurecav">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_currentwritespeed">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_donotfinalizemedia">get_DoNotFinalizeMedia</a>
</td>
<td align="left" width="63%">
Determines if the media is left open for writing after writing the audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_expectedtableofcontents">get_ExpectedTableOfContents</a>
</td>
<td align="left" width="63%">
Retrieves the table of content for the audio tracks that were laid on the media within the track-writing session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_freesectorsonmedia">get_FreeSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of sectors available for adding a new track to the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_numberofexistingtracks">get_NumberOfExistingTracks</a>
</td>
<td align="left" width="63%">
Retrieves the number of existing audio tracks on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_recorder">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_requestedrotationtypeispurecav">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_requestedwritespeed">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeddescriptors">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeds">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_totalsectorsonmedia">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total sectors available on the media if writing one continuous audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_usedsectorsonmedia">get_UsedSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total number of used sectors on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-preparemedia">PrepareMedia</a>
</td>
<td align="left" width="63%">
Locks the current media for exclusive access. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_bufferunderrunfreedisabled">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_clientname">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_donotfinalizemedia">put_DoNotFinalizeMedia</a>
</td>
<td align="left" width="63%">
Determines if the media is left open for writing after writing the audio track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_recorder">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">ReleaseMedia</a>
</td>
<td align="left" width="63%">
Closes the track-writing session and releases the lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-setwritespeed">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
</table>

## -remarks

To create the <b>MsftDiscFormat2TrackAtOnce</b> object in a script, use IMAPI2.MsftDiscFormat2TrackAtOnce as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://docs.microsoft.com/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>

