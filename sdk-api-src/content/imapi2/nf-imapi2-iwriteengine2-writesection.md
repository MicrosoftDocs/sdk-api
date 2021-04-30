---
UID: NF:imapi2.IWriteEngine2.WriteSection
title: IWriteEngine2::WriteSection (imapi2.h)
description: Writes a data stream to the current recorder.
helpviewer_keywords: ["IWriteEngine2 interface [IMAPI]","WriteSection method","IWriteEngine2.WriteSection","IWriteEngine2::WriteSection","WriteSection","WriteSection method [IMAPI]","WriteSection method [IMAPI]","IWriteEngine2 interface","imapi.iwriteengine2_writesection","imapi2/IWriteEngine2::WriteSection"]
old-location: imapi\iwriteengine2_writesection.htm
tech.root: imapi
ms.assetid: a6158984-04d3-4919-8a67-fc860b4b3a47
ms.date: 12/05/2018
ms.keywords: IWriteEngine2 interface [IMAPI],WriteSection method, IWriteEngine2.WriteSection, IWriteEngine2::WriteSection, WriteSection, WriteSection method [IMAPI], WriteSection method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_writesection, imapi2/IWriteEngine2::WriteSection
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
 - IWriteEngine2::WriteSection
 - imapi2/IWriteEngine2::WriteSection
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
 - IWriteEngine2.WriteSection
---

# IWriteEngine2::WriteSection


## -description

Writes a data stream to the current recorder.

## -parameters

### -param data [in]

An <b>IStream</b> interface of the data stream to write to the recorder.

### -param startingBlockAddress [in]

Starting logical block address (LBA) of the write operation. Negative values are supported.

### -param numberOfBlocks [in]

Number of blocks from the data stream to write.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_REQUEST_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was canceled.

Value: 0xC0AA0002

</td>
</tr>
</table>

## -remarks

Before calling this method, you must call the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_recorder">IWriteEngine2::put_Recorder</a> method to specify the recording device and the <a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_bytespersector">IWriteEngine2::put_BytesPerSector</a> method to specify the number of bytes to use for each sector during writing.

You should also consider calling the following methods if their default values are not appropriate for your application:

<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_endingsectorspersecond">IWriteEngine2::put_EndingSectorsPerSecond</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_startingsectorspersecond">IWriteEngine2::put_StartingSectorsPerSecond</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_usestreamingwrite12">IWriteEngine2::put_UseStreamingWrite12</a>
</li>
</ul>
This method is synchronous. To determine the progress of the write operation, you must implement the <a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a> interface. For examples that show how to implement an event handler in a script, see <a href="/windows/desktop/imapi/monitoring-progress-with-events">Monitoring Progress With Events</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2">IWriteEngine2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-cancelwrite">IWriteEngine2::CancelWrite</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-get_writeinprogress">IWriteEngine2::get_WriteInProgress</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_sectorcount">IWriteEngine2EventArgs::get_SectorCount</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2eventargs-get_startlba">IWriteEngine2EventArgs::get_StartLba</a>