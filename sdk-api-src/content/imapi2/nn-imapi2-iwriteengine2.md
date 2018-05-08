---
UID: NN:imapi2.IWriteEngine2
title: IWriteEngine2
author: windows-driver-content
description: Use this interface to write a data stream to a device.
old-location: imapi\iwriteengine2.htm
old-project: imapi
ms.assetid: 89e7526f-2b9b-4f37-b537-5046a0ac283d
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IWriteEngine2, IWriteEngine2 interface [IMAPI], IWriteEngine2 interface [IMAPI],described, imapi.iwriteengine2, imapi2/IWriteEngine2
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
-	IWriteEngine2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2 interface


## -description


Use this interface to write a data stream to a device.

This interface should be used by those  developing support for new media types or formats. Writing to media typically includes the following steps:<ol>
<li>Preparing the hardware by setting mode pages for the media.
</li>
<li>Querying the hardware to verify that the media is large enough.</li>
<li>Initializing the write, for example, by formatting the media or setting OPC.
</li>
<li>Performing the actual WRITE commands.</li>
<li>Finishing the write by stopping the formatting or closing the session or track.</li>
</ol>When developing support for new media types, you can implement steps 1, 2, 3, and 5, and use this interface to perform step 4. Note that all the IDiscFormat2* interfaces use this interface to perform the write operation.

Most client applications should use the <a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a> interface to write images to a device.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftWriteEngine2) for the class identifier and __uuidof(IWriteEngine2) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWriteEngine2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWriteEngine2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWriteEngine2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd658bd3-71ab-4e63-adec-8b7405a76c12">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels a write operation that is in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee48368c-e9bc-4ac7-97cf-a2bdc2a05d22">get_BytesPerSector</a>
</td>
<td align="left" width="63%">
Retrieves the logical block size of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e6a5f41-328d-47b3-ba43-900e524cf51a">get_EndingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the estimated speed at the end of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f42c5289-0896-4e2f-902e-9c6bdbf23b40">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use in the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/335da519-7378-469d-83dc-7c6a265fe67b">get_StartingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the estimated speed that the recording device can write to the media at the start of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28f5673e-73f4-4bec-bdee-49cbd030a0d6">get_UseStreamingWrite12</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the write operations use the WRITE12 or WRITE10 command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88f67eab-c87b-4a15-b29f-25675d0cac22">get_WriteInProgress</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the recorder is currently writing data to the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aac64c0a-4304-4a20-822e-4aa247d3d9e8">put_BytesPerSector</a>
</td>
<td align="left" width="63%">
Sets the logical block size of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7060578d-c6d5-4155-9ab8-7185bde38f64">put_EndingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Sets the estimated speed at the end of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ab46d99-7940-4ad0-9772-634de8c0d0ef">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets a recording device for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e">put_StartingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Sets the estimated speed that the recording device can write to the media at the start of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0fa6248-c582-423d-8983-81cd56d9abdd">put_UseStreamingWrite12</a>
</td>
<td align="left" width="63%">
Sets a value that indicates if the write operations use the WRITE12 or WRITE10 command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6158984-04d3-4919-8a67-fc860b4b3a47">WriteSection</a>
</td>
<td align="left" width="63%">
Writes a data stream to the current recorder.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftWriteEngine2</b> object in a script, use IMAPI2.MsftWriteEngine2 as the program identifier when calling <b>CreateObject</b>.

 It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://msdn.microsoft.com/5223c9f6-30f6-43ce-b46c-267da0a53d4b">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://msdn.microsoft.com/697f8247-6940-4b5e-8521-df89838837be">DWriteEngine2Events</a>



<a href="https://msdn.microsoft.com/c0bc2e8b-bd60-4c97-bd86-41963b20b1a3">IDiscFormat2</a>



<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>



<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>
 

 

