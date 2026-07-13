---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfileId
title: IConfigAsfWriter::GetCurrentProfileId (dshowasf.h)
description: The GetCurrentProfileId method retrieves the identifier of the WM ASF Writer filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.).
helpviewer_keywords: ["GetCurrentProfileId","GetCurrentProfileId method [DirectShow]","GetCurrentProfileId method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","GetCurrentProfileId method","IConfigAsfWriter.GetCurrentProfileId","IConfigAsfWriter::GetCurrentProfileId","IConfigAsfWriterGetCurrentProfileId","dshow.iconfigasfwriter_getcurrentprofileid","dshowasf/IConfigAsfWriter::GetCurrentProfileId"]
old-location: dshow\iconfigasfwriter_getcurrentprofileid.htm
tech.root: dshow
ms.assetid: 37288625-368f-41d4-bfdc-bb2fd144f455
ms.date: 4/26/2023
ms.keywords: GetCurrentProfileId, GetCurrentProfileId method [DirectShow], GetCurrentProfileId method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfileId method, IConfigAsfWriter.GetCurrentProfileId, IConfigAsfWriter::GetCurrentProfileId, IConfigAsfWriterGetCurrentProfileId, dshow.iconfigasfwriter_getcurrentprofileid, dshowasf/IConfigAsfWriter::GetCurrentProfileId
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
 - IConfigAsfWriter::GetCurrentProfileId
 - dshowasf/IConfigAsfWriter::GetCurrentProfileId
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
 - IConfigAsfWriter.GetCurrentProfileId
---

# IConfigAsfWriter::GetCurrentProfileId


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentProfileId</code> method retrieves the identifier of the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.)

## -parameters

### -param pdwProfileId [out]

Receives the current profile ID.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.

## -remarks

This method is obsolete because it applies only to version 4.0 Windows Media Format SDK profiles. Applications should call <a href="/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-getcurrentprofile">IConfigAsfWriter::GetCurrentProfile</a> to get the current profile.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>