---
UID: NN:imapi2.IDiscFormat2Data
title: IDiscFormat2Data (imapi2.h)
description: Use this interface to write a data stream to a disc.
helpviewer_keywords: ["IDiscFormat2Data","IDiscFormat2Data interface [IMAPI]","IDiscFormat2Data interface [IMAPI]","described","imapi.idiscformat2data","imapi2/IDiscFormat2Data"]
old-location: imapi\idiscformat2data.htm
tech.root: imapi
ms.assetid: 6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data, IDiscFormat2Data interface [IMAPI], IDiscFormat2Data interface [IMAPI],described, imapi.idiscformat2data, imapi2/IDiscFormat2Data
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
 - IDiscFormat2Data
 - imapi2/IDiscFormat2Data
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
 - IDiscFormat2Data
---

# IDiscFormat2Data interface


## -description

Use this interface to write a data stream to a disc.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2Data) for the class identifier and __uuidof(IDiscFormat2Data) for the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2Data</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2Data</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2Data</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-cancelwrite">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels the current write operation. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_bufferunderrunfreedisabled">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_clientname">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentmediastatus">get_CurrentMediaStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentphysicalmediatype">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentrotationtypeispurecav">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentwritespeed">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_disableconsumerdvdcompatibilitymode">get_DisableConsumerDvdCompatibilityMode</a>
</td>
<td align="left" width="63%">
Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_forcemediatobeclosed">get_ForceMediaToBeClosed</a>
</td>
<td align="left" width="63%">
Determines if further additions to the file system are prevented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_forceoverwrite">get_ForceOverwrite</a>
</td>
<td align="left" width="63%">
Determines if the data writer must overwrite the disc on overwritable media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_freesectorsonmedia">get_FreeSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of free sectors on the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_lastwrittenaddressofprevioussession">get_LastWrittenAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the last sector of the previous write session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">get_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves a list of available multi-session interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_nextwritableaddress">get_NextWritableAddress</a>
</td>
<td align="left" width="63%">
Retrieves the location for the next write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_postgapalreadyinimage">get_PostgapAlreadyInImage</a>
</td>
<td align="left" width="63%">
Determines if the data stream contains post-writing gaps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_recorder">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_requestedrotationtypeispurecav">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_requestedwritespeed">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_startaddressofprevioussession">get_StartAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the first sector of the previous write session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_supportedwritespeeddescriptors">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_supportedwritespeeds">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_totalsectorsonmedia">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of sectors on the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_writeprotectstatus">get_WriteProtectStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current write protect state of the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_bufferunderrunfreedisabled">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_clientname">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_disableconsumerdvdcompatibilitymode">put_DisableConsumerDvdCompatibilityMode</a>
</td>
<td align="left" width="63%">
Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_forcemediatobeclosed">put_ForceMediaToBeClosed</a>
</td>
<td align="left" width="63%">
Determines if further additions to the file system are prevented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_forceoverwrite">put_ForceOverwrite</a>
</td>
<td align="left" width="63%">
Determines if the data writer must overwrite the disc on overwritable media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_postgapalreadyinimage">put_PostgapAlreadyInImage</a>
</td>
<td align="left" width="63%">
Determines if the data stream contains post-writing gaps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-setwritespeed">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write">Write</a>
</td>
<td align="left" width="63%">
Writes the data stream to the device.

</td>
</tr>
</table>

## -remarks

To create the <b>MsftDiscFormat2Data</b> object in a script, use IMAPI2.MsftDiscFormat2Data as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://docs.microsoft.com/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>

