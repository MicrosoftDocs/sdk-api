---
UID: NN:imapi2.IDiscFormat2RawCD
title: IDiscFormat2RawCD
author: windows-sdk-content
description: Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording).
old-location: imapi\idiscformat2rawcd.htm
tech.root: imapi
ms.assetid: 58d9b83c-a528-4b39-b08d-a0fb8c1aece8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2RawCD, IDiscFormat2RawCD interface [IMAPI], IDiscFormat2RawCD interface [IMAPI],described, imapi.idiscformat2rawcd, imapi2/IDiscFormat2RawCD
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCD interface


## -description


Use this interface to write raw images to a disc device using Disc At Once (DAO) mode (also known as uninterrupted recording). For information on DAO mode, see the latest revision of the MMC specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=83843">ftp://ftp.t10.org/t10/drafts/mmc5</a>.  

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2RawCD) for the class identifier and __uuidof(IDiscFormat2RawCD) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2RawCD</b> interface inherits from <a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>. <b>IDiscFormat2RawCD</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12cd6797-dcb8-496d-a141-9d3a805266e9">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels the current write operation. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85b20760-334e-47a1-9683-be3d76c8958f">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd706b68-0dde-4a44-b5f5-764fad56844f">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76fae45e-c58a-4a25-a2d2-ec99c12374b9">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca3ab4e3-e87c-4081-bb65-c1d8c3f1ff37">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f369f719-7db6-4a79-a5fa-d174bf12acbc">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2588f35e-388b-4491-a209-99d34b1d82df">get_LastPossibleStartOfLeadout</a>
</td>
<td align="left" width="63%">
Retrieves the last possible starting position for the leadout area.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f36e5b5-4875-4ba1-8084-c0aaf6b170b9">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/884624e2-96d7-491a-add3-a5bd3edc473e">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7964e25e-43ed-4ed0-aeee-dac656700fea">get_RequestedSectorType</a>
</td>
<td align="left" width="63%">
Retrieves the requested data sector to use during write of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b718fe5-197e-4dc7-a8df-f2febf76aaab">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9ffe037-c7a6-40c2-a809-58dbfd9e7415">get_StartOfNextSession</a>
</td>
<td align="left" width="63%">
Retrieves the first sector of the next session.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d217e585-3ff4-4f02-8a13-7cfca767f201">get_SupportedSectorTypes</a>
</td>
<td align="left" width="63%">
Retrieves the supported data sector types for the current recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00a7c10a-7790-4193-928c-d3211047dbbe">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ebcc42f-d864-407f-a1a6-d4811ca8221c">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c393786-0c2d-4244-8ec3-0ac9e47e76c6">PrepareMedia</a>
</td>
<td align="left" width="63%">
Locks the current media for exclusive access. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66b35ca9-2bc7-419e-8fff-4449a64f9f5f">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49fce259-2b39-4905-a48f-a252537d8360">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3deefa8-40be-4cdc-aae1-e5fbe508f16f">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd9d7e1d-5672-482f-ac83-efcab3adbac4">put_RequestedSectorType</a>
</td>
<td align="left" width="63%">
Sets the requested data sector to use for writing of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f60c16f-ef40-4bb5-8df2-fa4ae91541b6">ReleaseMedia</a>
</td>
<td align="left" width="63%">
Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/137395f1-b0cf-4bd0-9d3b-a21122eb8b57">WriteMedia</a>
</td>
<td align="left" width="63%">
Writes a DAO-96 raw image to the blank media using MSF 95:00:00 as the starting address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/636d04dd-081d-407c-827e-55e443516d9b">WriteMedia2</a>
</td>
<td align="left" width="63%">
Writes a DAO-96 raw image to the blank media using a specified starting address.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscFormat2RawCD</b> object in a script, use IMAPI2.MsftDiscFormat2RawCD as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://msdn.microsoft.com/5223c9f6-30f6-43ce-b46c-267da0a53d4b">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>
 

 

