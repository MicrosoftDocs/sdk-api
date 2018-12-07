---
UID: NN:imapi2.IDiscFormat2Data
title: IDiscFormat2Data
author: windows-sdk-content
description: Use this interface to write a data stream to a disc.
old-location: imapi\idiscformat2data.htm
tech.root: imapi
ms.assetid: 6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2Data, IDiscFormat2Data interface [IMAPI], IDiscFormat2Data interface [IMAPI],described, imapi.idiscformat2data, imapi2/IDiscFormat2Data
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
 - IDiscFormat2Data
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Data interface


## -description


Use this interface to write a data stream to a disc.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2Data) for the class identifier and __uuidof(IDiscFormat2Data) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2Data</b> interface inherits from <a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>. <b>IDiscFormat2Data</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0fe5705e-7f48-4a4e-a535-a3dd105a6139">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels the current write operation. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b85f13c-33c2-4b19-9b70-5a829f9de3ea">get_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/faf5009a-395a-49ed-a0c7-e6bc44f17b7c">get_ClientName</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8ed119f-8976-48aa-ab9a-86c1361b6e14">get_CurrentMediaStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b9a80fc-6ef5-4102-9361-313d33f182ab">get_CurrentPhysicalMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the type of media in the disc device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4740a631-d5e1-496a-9631-0398a7709319">get_CurrentRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the rotational-speed control used by the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec087250-3c95-4d08-a5c5-21ff0d7f64a1">get_CurrentWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the drive's current write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc88f657-0ec1-488d-8110-055de06c2d58">get_DisableConsumerDvdCompatibilityMode</a>
</td>
<td align="left" width="63%">
Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9de0afa9-93b7-4a12-b8e2-a9c083692f98">get_ForceMediaToBeClosed</a>
</td>
<td align="left" width="63%">
Determines if further additions to the file system are prevented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac1bfca7-e681-4e88-85d6-c77ffcbe7872">get_ForceOverwrite</a>
</td>
<td align="left" width="63%">
Determines if the data writer must overwrite the disc on overwritable media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33313831-859c-4e35-9a43-cde2220b43d1">get_FreeSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of free sectors on the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfc9ba42-25a2-49a3-8047-7aaf331332ad">get_LastWrittenAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the last sector of the previous write session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bb2d100-629f-4b63-a699-ddce85213e72">get_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves a list of available multi-session interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdbab74c-80bd-4dca-8d64-6d30452a5876">get_NextWritableAddress</a>
</td>
<td align="left" width="63%">
Retrieves the location for the next write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f4423b8-8cda-4ef2-a8f6-4ef7e147bf6b">get_PostgapAlreadyInImage</a>
</td>
<td align="left" width="63%">
Determines if the data stream contains post-writing gaps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313ba824-b54a-4b3a-a669-49067c71798d">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edf3a5a7-3164-4fba-bbbe-525932b0284d">get_RequestedRotationTypeIsPureCAV</a>
</td>
<td align="left" width="63%">
Retrieves the requested rotational-speed control type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7db85ce1-ff93-4bda-8245-3ffe85e835d3">get_RequestedWriteSpeed</a>
</td>
<td align="left" width="63%">
Retrieves the requested write speed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2f75240-9334-42a3-82d6-5ce9ddf1f3a2">get_StartAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the first sector of the previous write session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eb84ec6-900a-45ba-9111-9c9c6b3f5bb2">get_SupportedWriteSpeedDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of the detailed write configurations supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09d8019d-b3d5-47e1-8fda-58c542d5829d">get_SupportedWriteSpeeds</a>
</td>
<td align="left" width="63%">
Retrieves a list of the write speeds supported by the disc recorder and current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ad23657-36db-4edd-841d-eecb591209f5">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of sectors on the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3e58024-9a51-46e9-a9a1-c850166c9a85">get_WriteProtectStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current write protect state of the media in the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32d05abe-c434-4a87-b6ee-961a999321c5">put_BufferUnderrunFreeDisabled</a>
</td>
<td align="left" width="63%">
Determines if Buffer Underrun Free Recording is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cd4ef46-4769-4e8e-80ca-fdcd81b486f1">put_ClientName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the client. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d32bbb33-0cb6-46cd-8a06-7ddd6e94a7b3">put_DisableConsumerDvdCompatibilityMode</a>
</td>
<td align="left" width="63%">
Determines if a DVD recording session includes tasks that can increase the chance that a device can play the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a087a73-1b61-481d-8deb-a251511906a9">put_ForceMediaToBeClosed</a>
</td>
<td align="left" width="63%">
Determines if further additions to the file system are prevented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b77c94-ad2a-42c8-8042-267a48036dac">put_ForceOverwrite</a>
</td>
<td align="left" width="63%">
Determines if the data writer must overwrite the disc on overwritable media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68dba44b-ac14-4473-9b74-917ce2c5054a">put_PostgapAlreadyInImage</a>
</td>
<td align="left" width="63%">
Determines if the data stream contains post-writing gaps.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8d1f6ec-09cb-4144-b44c-970555451aee">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets the recording device to use for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3e03af5-bda2-49a3-80d9-52acfe390708">SetWriteSpeed</a>
</td>
<td align="left" width="63%">
Sets the write speed of the attached disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9daf31f3-84c2-48b2-ab21-a3809b6ed9af">Write</a>
</td>
<td align="left" width="63%">
Writes the data stream to the device.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftDiscFormat2Data</b> object in a script, use IMAPI2.MsftDiscFormat2Data as the program identifier when calling <b>CreateObject</b>.

It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://msdn.microsoft.com/5223c9f6-30f6-43ce-b46c-267da0a53d4b">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>



<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>



<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>
 

 

