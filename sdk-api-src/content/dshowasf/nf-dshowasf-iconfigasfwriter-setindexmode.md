---
UID: NF:dshowasf.IConfigAsfWriter.SetIndexMode
title: IConfigAsfWriter::SetIndexMode (dshowasf.h)
description: The SetIndexMode method controls whether the WM ASF Writer filter creates a file with a temporal index.
helpviewer_keywords: ["IConfigAsfWriter interface [DirectShow]","SetIndexMode method","IConfigAsfWriter.SetIndexMode","IConfigAsfWriter::SetIndexMode","IConfigAsfWriterSetIndexMode","SetIndexMode","SetIndexMode method [DirectShow]","SetIndexMode method [DirectShow]","IConfigAsfWriter interface","dshow.iconfigasfwriter_setindexmode","dshowasf/IConfigAsfWriter::SetIndexMode"]
old-location: dshow\iconfigasfwriter_setindexmode.htm
tech.root: dshow
ms.assetid: d7f5d13a-d36e-4da2-babc-0446e5697b61
ms.date: 4/26/2023
ms.keywords: IConfigAsfWriter interface [DirectShow],SetIndexMode method, IConfigAsfWriter.SetIndexMode, IConfigAsfWriter::SetIndexMode, IConfigAsfWriterSetIndexMode, SetIndexMode, SetIndexMode method [DirectShow], SetIndexMode method [DirectShow],IConfigAsfWriter interface, dshow.iconfigasfwriter_setindexmode, dshowasf/IConfigAsfWriter::SetIndexMode
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
 - IConfigAsfWriter::SetIndexMode
 - dshowasf/IConfigAsfWriter::SetIndexMode
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
 - IConfigAsfWriter.SetIndexMode
---

# IConfigAsfWriter::SetIndexMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetIndexMode</code> method controls whether the WM ASF Writer filter creates a file with a temporal index.

## -parameters

### -param bIndexFile [in]

Specifies the index mode. If <b>TRUE</b>, the file will be indexed.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.

## -remarks

By default, the WM ASF Writer filter creates temporally indexed ASF files. It performs the indexing when the graph stops. You can disable this behavior if you want to do your own frame-based indexing as a post-processing step. To create a frame-indexed file, call <code>SetIndexMode</code> with the value <b>FALSE</b>, create the file, and then use the Windows Media Format SDK methods to create a frame-based index for the file.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>