---
UID: NF:mfreadwrite.MFCreateSourceReaderFromMediaSource
title: MFCreateSourceReaderFromMediaSource function (mfreadwrite.h)
description: Creates the source reader from a media source.
helpviewer_keywords: ["MFCreateSourceReaderFromMediaSource","MFCreateSourceReaderFromMediaSource function [Media Foundation]","mf.mfcreatesourcereaderfrommediasource","mfreadwrite/MFCreateSourceReaderFromMediaSource"]
old-location: mf\mfcreatesourcereaderfrommediasource.htm
tech.root: mf
ms.assetid: 924e1813-b025-435b-9770-52503a9eb619
ms.date: 12/05/2018
ms.keywords: MFCreateSourceReaderFromMediaSource, MFCreateSourceReaderFromMediaSource function [Media Foundation], mf.mfcreatesourcereaderfrommediasource, mfreadwrite/MFCreateSourceReaderFromMediaSource
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSourceReaderFromMediaSource
 - mfreadwrite/MFCreateSourceReaderFromMediaSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfreadwrite.dll
api_name:
 - MFCreateSourceReaderFromMediaSource
---

# MFCreateSourceReaderFromMediaSource function


## -description

Creates the source reader from a media source.

## -parameters

### -param pMediaSource [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface of a media source.

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="/windows/desktop/medfound/source-reader-attributes">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.

### -param ppSourceReader [out]

Receives a pointer to the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_DRM_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The source contains protected content.

</td>
</tr>
</table>

## -remarks

Call <b>CoInitialize(Ex)</b> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> before calling this function.

By default, when the application releases the source reader, the source reader shuts down the media source by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">IMFMediaSource::Shutdown</a> on the media source. At that point, the application can no longer use the media source.

To change this default behavior, set the <a href="/windows/desktop/medfound/mf-source-reader-disconnect-mediasource-on-shutdown">MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN</a> attribute in the <i>pAttributes</i> parameter. If this attribute is <b>TRUE</b>, the application is responsible for  shutting down the media source.

When using the Source Reader, do not call any of the following methods on the media source:<ul>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause">IMFMediaSource::Pause</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start">IMFMediaSource::Start</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop">IMFMediaSource::Stop</a>
</li>
<li>All <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> methods</li>
</ul>


This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>