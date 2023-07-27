---
UID: NF:dshowasf.IConfigAsfWriter2.GetParam
title: IConfigAsfWriter2::GetParam (dshowasf.h)
description: The GetParam method retrieves the current value of the specified filter configuration parameter.
helpviewer_keywords: ["GetParam","GetParam method [DirectShow]","GetParam method [DirectShow]","IConfigAsfWriter2 interface","IConfigAsfWriter2 interface [DirectShow]","GetParam method","IConfigAsfWriter2.GetParam","IConfigAsfWriter2::GetParam","IConfigAsfWriter2GetParam","dshow.iconfigasfwriter2_getparam","dshowasf/IConfigAsfWriter2::GetParam"]
old-location: dshow\iconfigasfwriter2_getparam.htm
tech.root: dshow
ms.assetid: 2a875d02-3814-46a1-9eee-61bad36475fc
ms.date: 4/26/2023
ms.keywords: GetParam, GetParam method [DirectShow], GetParam method [DirectShow],IConfigAsfWriter2 interface, IConfigAsfWriter2 interface [DirectShow],GetParam method, IConfigAsfWriter2.GetParam, IConfigAsfWriter2::GetParam, IConfigAsfWriter2GetParam, dshow.iconfigasfwriter2_getparam, dshowasf/IConfigAsfWriter2::GetParam
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IConfigAsfWriter2::GetParam
 - dshowasf/IConfigAsfWriter2::GetParam
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
 - IConfigAsfWriter2.GetParam
---

# IConfigAsfWriter2::GetParam


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetParam</code> method retrieves the current value of the specified filter configuration parameter.

## -parameters

### -param dwParam [in]

Specifies the parameter to retrieve, as a member of the <a href="/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)">_AM_ASFWRITERCONFIG_PARAM</a> enumeration.

### -param pdwParam1 [out]

Receives the value of the parameter specified in <i>dwParam</i>.

### -param pdwParam2 [out]

Reserved. Must be zero.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2">IConfigAsfWriter2 Interface</a>