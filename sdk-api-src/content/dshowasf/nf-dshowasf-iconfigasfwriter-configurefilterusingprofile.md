---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfile
title: IConfigAsfWriter::ConfigureFilterUsingProfile (dshowasf.h)
description: The ConfigureFilterUsingProfile method sets an ASF profile on the WM ASF Writer filter. This method is the recommended way to set a profile on the WM ASF Writer filter.
helpviewer_keywords: ["ConfigureFilterUsingProfile","ConfigureFilterUsingProfile method [DirectShow]","ConfigureFilterUsingProfile method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","ConfigureFilterUsingProfile method","IConfigAsfWriter.ConfigureFilterUsingProfile","IConfigAsfWriter::ConfigureFilterUsingProfile","IConfigAsfWriterConfigureFilterUsingProfile","dshow.iconfigasfwriter_configurefilterusingprofile","dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile"]
old-location: dshow\iconfigasfwriter_configurefilterusingprofile.htm
tech.root: dshow
ms.assetid: 89156f64-7a20-4226-9f01-5b1bd4a1fe98
ms.date: 4/26/2023
ms.keywords: ConfigureFilterUsingProfile, ConfigureFilterUsingProfile method [DirectShow], ConfigureFilterUsingProfile method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfile method, IConfigAsfWriter.ConfigureFilterUsingProfile, IConfigAsfWriter::ConfigureFilterUsingProfile, IConfigAsfWriterConfigureFilterUsingProfile, dshow.iconfigasfwriter_configurefilterusingprofile, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IConfigAsfWriter::ConfigureFilterUsingProfile
 - dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.ConfigureFilterUsingProfile
---

# IConfigAsfWriter::ConfigureFilterUsingProfile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ConfigureFilterUsingProfile</code> method sets an ASF profile on the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. This method is the recommended way to set a profile on the WM ASF Writer filter.

## -parameters

### -param pProfile [in]

Pointer to the <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface of the profile.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The graph is stopped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface pointer is invalid.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface is documented in the Windows Media Format SDK.

If successful, this method will cause an <a href="/windows/desktop/DirectShow/ec-graph-changed">EC_GRAPH_CHANGED</a> event to be sent to the application.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>