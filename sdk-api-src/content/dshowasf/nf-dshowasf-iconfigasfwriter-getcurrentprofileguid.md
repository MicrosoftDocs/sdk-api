---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfileGuid
title: IConfigAsfWriter::GetCurrentProfileGuid (dshowasf.h)
description: The GetCurrentProfileGuid method retrieves the GUID of the WM ASF Writer filter's current system profile, if any. (Deprecated.).
helpviewer_keywords: ["GetCurrentProfileGuid","GetCurrentProfileGuid method [DirectShow]","GetCurrentProfileGuid method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","GetCurrentProfileGuid method","IConfigAsfWriter.GetCurrentProfileGuid","IConfigAsfWriter::GetCurrentProfileGuid","IConfigAsfWriterGetCurrentProfileGuid","dshow.iconfigasfwriter_getcurrentprofileguid","dshowasf/IConfigAsfWriter::GetCurrentProfileGuid"]
old-location: dshow\iconfigasfwriter_getcurrentprofileguid.htm
tech.root: dshow
ms.assetid: 8958f8d3-40ff-44b1-a817-5dca30636306
ms.date: 4/26/2023
ms.keywords: GetCurrentProfileGuid, GetCurrentProfileGuid method [DirectShow], GetCurrentProfileGuid method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfileGuid method, IConfigAsfWriter.GetCurrentProfileGuid, IConfigAsfWriter::GetCurrentProfileGuid, IConfigAsfWriterGetCurrentProfileGuid, dshow.iconfigasfwriter_getcurrentprofileguid, dshowasf/IConfigAsfWriter::GetCurrentProfileGuid
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
 - IConfigAsfWriter::GetCurrentProfileGuid
 - dshowasf/IConfigAsfWriter::GetCurrentProfileGuid
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
 - IConfigAsfWriter.GetCurrentProfileGuid
---

# IConfigAsfWriter::GetCurrentProfileGuid


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentProfileGuid</code> method retrieves the GUID of the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter's current system profile, if any. (Deprecated.)

## -parameters

### -param pProfileGuid [out]

Receives the <b>GUID</b> of the system profile.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.

## -remarks

This method applies only when the WM ASF Writer filter is configured with a system profile. If the application provided its own ASF profile instead of a system profile (as is recommended), the profile GUID is GUID_NULL. Applications should call <a href="/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-getcurrentprofile">IConfigAsfWriter::GetCurrentProfile</a> to get the current profile.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>