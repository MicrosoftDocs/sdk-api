---
UID: NF:mfapi.MFCreateMediaEvent
title: MFCreateMediaEvent function (mfapi.h)
description: Creates a media event object.
helpviewer_keywords: ["64da695e-5f56-4f23-9a06-0b0c358e3cc3","MFCreateMediaEvent","MFCreateMediaEvent function [Media Foundation]","mf.mfcreatemediaevent","mfapi/MFCreateMediaEvent"]
old-location: mf\mfcreatemediaevent.htm
tech.root: mf
ms.assetid: 64da695e-5f56-4f23-9a06-0b0c358e3cc3
ms.date: 12/05/2018
ms.keywords: 64da695e-5f56-4f23-9a06-0b0c358e3cc3, MFCreateMediaEvent, MFCreateMediaEvent function [Media Foundation], mf.mfcreatemediaevent, mfapi/MFCreateMediaEvent
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMediaEvent
 - mfapi/MFCreateMediaEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMediaEvent
---

# MFCreateMediaEvent function


## -description

Creates a media event object.

## -parameters

### -param met

The event type. See <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype">IMFMediaEvent::GetType</a>. For a list of event types, see <a href="/windows/desktop/medfound/media-foundation-events">Media Foundation Events</a>.

### -param guidExtendedType

The extended type. See <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype">IMFMediaEvent::GetExtendedType</a>. If the event type does not have an extended type, use the value GUID_NULL.

### -param hrStatus

The event status. See <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus">IMFMediaEvent::GetStatus</a>

### -param pvValue

The value associated with the event, if any. See <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue">IMFMediaEvent::GetValue</a>. This parameter can be <b>NULL</b>.

### -param ppEvent

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>