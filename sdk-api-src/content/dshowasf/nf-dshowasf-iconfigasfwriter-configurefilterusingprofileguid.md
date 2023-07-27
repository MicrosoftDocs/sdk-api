---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfileGuid
title: IConfigAsfWriter::ConfigureFilterUsingProfileGuid (dshowasf.h)
description: The ConfigureFilterUsingProfileGuid method sets a predefined system profile on the WM ASF Writer filter. This method is deprecated. Applications should use the IConfigAsfWriter::ConfigureFilterUsingProfile method to set the profile.
helpviewer_keywords: ["ConfigureFilterUsingProfileGuid","ConfigureFilterUsingProfileGuid method [DirectShow]","ConfigureFilterUsingProfileGuid method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","ConfigureFilterUsingProfileGuid method","IConfigAsfWriter.ConfigureFilterUsingProfileGuid","IConfigAsfWriter::ConfigureFilterUsingProfileGuid","IConfigAsfWriterConfigureFilterUsingProfileGuid","dshow.iconfigasfwriter_configurefilterusingprofileguid","dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileGuid"]
old-location: dshow\iconfigasfwriter_configurefilterusingprofileguid.htm
tech.root: dshow
ms.assetid: 8cfb3b22-aa6b-42e0-bbb5-876932e8bd82
ms.date: 4/26/2023
ms.keywords: ConfigureFilterUsingProfileGuid, ConfigureFilterUsingProfileGuid method [DirectShow], ConfigureFilterUsingProfileGuid method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfileGuid method, IConfigAsfWriter.ConfigureFilterUsingProfileGuid, IConfigAsfWriter::ConfigureFilterUsingProfileGuid, IConfigAsfWriterConfigureFilterUsingProfileGuid, dshow.iconfigasfwriter_configurefilterusingprofileguid, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileGuid
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
 - IConfigAsfWriter::ConfigureFilterUsingProfileGuid
 - dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileGuid
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
 - IConfigAsfWriter.ConfigureFilterUsingProfileGuid
---

# IConfigAsfWriter::ConfigureFilterUsingProfileGuid


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ConfigureFilterUsingProfileGuid</code> method sets a predefined system profile on the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. This method is deprecated. Applications should use the <a href="/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile">IConfigAsfWriter::ConfigureFilterUsingProfile</a> method to set the profile.

## -parameters

### -param guidProfile [in]

Profile <b>GUID</b> as defined in the header file Wmsysprf.h.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is stopped.

</td>
</tr>
</table>

## -remarks

Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined. Only version 8 (or earlier) system profile GUIDs can be used with this method.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>