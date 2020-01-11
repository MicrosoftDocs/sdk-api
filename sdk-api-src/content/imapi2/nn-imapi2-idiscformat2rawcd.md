---
UID: NN:imapi2.IDiscFormat2RawCD
title: IDiscFormat2RawCD (imapi2.h)
description: Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording).
old-location: imapi\idiscformat2rawcd.htm
tech.root: imapi
ms.assetid: 58d9b83c-a528-4b39-b08d-a0fb8c1aece8
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD, IDiscFormat2RawCD interface [IMAPI], IDiscFormat2RawCD interface [IMAPI],described, imapi.idiscformat2rawcd, imapi2/IDiscFormat2RawCD
f1_keywords:
- imapi2/IDiscFormat2RawCD
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- imapi2.h
api_name:
- IDiscFormat2RawCD
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscFormat2RawCD interface


## -description


Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording). For information on DAO mode, see the latest revision of the MMC specification at ftp://ftp.t10.org/t10/drafts/mmc5.  

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2RawCD) for the class identifier and __uuidof(IDiscFormat2RawCD) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2RawCD</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2RawCD</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2RawCD</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-cancelwrite">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels the current write operation. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_bufferunderrunfreedisabled">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_clientname">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_currentphysicalmediatype">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_currentrotationtypeispurecav">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_currentwritespeed">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_lastpossiblestartofleadout">get_LastPossibleStartOfLeadout</a>
</td>
<td align="left" width="63%">
Retrieves the last possible starting position for the leadout area.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_recorder">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_requestedrotationtypeispurecav">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_requestedsectortype">get_RequestedSectorType</a>
</td>
<td align="left" width="63%">
Retrieves the requested data sector to use during write of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_requestedwritespeed">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_startofnextsession">get_StartOfNextSession</a>
</td>
<td align="left" width="63%">
Retrieves the first sector of the next session.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedsectortypes">get_SupportedSectorTypes</a>
</td>
<td align="left" width="63%">
Retrieves the supported data sector types for the current recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedwritespeeddescriptors">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedwritespeeds">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-preparemedia">PrepareMedia</a>
</td>
<td align="left" width="63%">
Locks the current media for exclusive access. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_bufferunderrunfreedisabled">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_clientname">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_recorder">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_requestedsectortype">put_RequestedSectorType</a>
</td>
<td align="left" width="63%">
Sets the requested data sector to use for writing of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-releasemedia">ReleaseMedia</a>
</td>
<td align="left" width="63%">
Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-setwritespeed">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia">WriteMedia</a>
</td>
<td align="left" width="63%">
Writes a DAO-96 raw image to the blank media using MSF 95:00:00 as the starting address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia2">WriteMedia2</a>
</td>
<td align="left" width="63%">
Writes a DAO-96 raw image to the blank media using a specified starting address.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscFormat2RawCD</b> object in a script, use IMAPI2.MsftDiscFormat2RawCD as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://docs.microsoft.com/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>
 

 

