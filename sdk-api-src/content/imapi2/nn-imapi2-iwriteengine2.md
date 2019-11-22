---
UID: NN:imapi2.IWriteEngine2
title: IWriteEngine2 (imapi2.h)

description: Use this interface to write a data stream to a device.
old-location: imapi\iwriteengine2.htm
tech.root: imapi
ms.assetid: 89e7526f-2b9b-4f37-b537-5046a0ac283d

ms.date: 12/05/2018
ms.keywords: IWriteEngine2, IWriteEngine2 interface [IMAPI], IWriteEngine2 interface [IMAPI],described, imapi.iwriteengine2, imapi2/IWriteEngine2
ms.topic: interface
f1_keywords: 
 - "imapi2/IWriteEngine2"
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
 - IWriteEngine2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Most client applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface to write images to a device.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftWriteEngine2) for the class identifier and __uuidof(IWriteEngine2) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWriteEngine2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWriteEngine2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-cancelwrite">CancelWrite</a>
</td>
<td align="left" width="63%">
Cancels a write operation that is in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_bytespersector">get_BytesPerSector</a>
</td>
<td align="left" width="63%">
Retrieves the logical block size of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_endingsectorspersecond">get_EndingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the estimated speed at the end of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_recorder">get_Recorder</a>
</td>
<td align="left" width="63%">
Retrieves the recording device to use in the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_startingsectorspersecond">get_StartingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Retrieves the estimated speed that the recording device can write to the media at the start of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_usestreamingwrite12">get_UseStreamingWrite12</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the write operations use the WRITE12 or WRITE10 command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_writeinprogress">get_WriteInProgress</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the recorder is currently writing data to the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">put_BytesPerSector</a>
</td>
<td align="left" width="63%">
Sets the logical block size of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">put_EndingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Sets the estimated speed at the end of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_recorder">put_Recorder</a>
</td>
<td align="left" width="63%">
Sets a recording device for the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_startingsectorspersecond">put_StartingSectorsPerSecond</a>
</td>
<td align="left" width="63%">
Sets the estimated speed that the recording device can write to the media at the start of the writing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_usestreamingwrite12">put_UseStreamingWrite12</a>
</td>
<td align="left" width="63%">
Sets a value that indicates if the write operations use the WRITE12 or WRITE10 command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-writesection">WriteSection</a>
</td>
<td align="left" width="63%">
Writes a data stream to the current recorder.

</td>
</tr>
</table> 


## -remarks



To create the <b>MsftWriteEngine2</b> object in a script, use IMAPI2.MsftWriteEngine2 as the program identifier when calling <b>CreateObject</b>.

 It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the  interruption of the burn process and  possible data loss. For programming considerations, see <a href="https://docs.microsoft.com/windows/desktop/imapi/preventing-logoff-or-suspend-during-a-burn">Preventing Logoff or Suspend During a Burn</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs">IWriteEngine2EventArgs</a>
 

 

