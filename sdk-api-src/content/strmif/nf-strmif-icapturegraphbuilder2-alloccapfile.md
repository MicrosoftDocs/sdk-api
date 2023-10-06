---
UID: NF:strmif.ICaptureGraphBuilder2.AllocCapFile
title: ICaptureGraphBuilder2::AllocCapFile (strmif.h)
description: The AllocCapFile method preallocates a capture file to a specified size. For best results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.
helpviewer_keywords: ["AllocCapFile","AllocCapFile method [DirectShow]","AllocCapFile method [DirectShow]","ICaptureGraphBuilder2 interface","ICaptureGraphBuilder2 interface [DirectShow]","AllocCapFile method","ICaptureGraphBuilder2.AllocCapFile","ICaptureGraphBuilder2::AllocCapFile","ICaptureGraphBuilder2AllocCapFile","dshow.icapturegraphbuilder2_alloccapfile","strmif/ICaptureGraphBuilder2::AllocCapFile"]
old-location: dshow\icapturegraphbuilder2_alloccapfile.htm
tech.root: dshow
ms.assetid: e61459bd-cccb-4857-b336-82d23135fa16
ms.date: 4/26/2023
ms.keywords: AllocCapFile, AllocCapFile method [DirectShow], AllocCapFile method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],AllocCapFile method, ICaptureGraphBuilder2.AllocCapFile, ICaptureGraphBuilder2::AllocCapFile, ICaptureGraphBuilder2AllocCapFile, dshow.icapturegraphbuilder2_alloccapfile, strmif/ICaptureGraphBuilder2::AllocCapFile
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICaptureGraphBuilder2::AllocCapFile
 - strmif/ICaptureGraphBuilder2::AllocCapFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICaptureGraphBuilder2.AllocCapFile
---

# ICaptureGraphBuilder2::AllocCapFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AllocCapFile</code> method preallocates a capture file to a specified size. For best results, always capture to a defragmented, preallocated capture file that is larger than the size of the capture data.

## -parameters

### -param lpstr [in]

Pointer to a wide-character string that contains the name of the file to create or resize.

### -param dwlSize [in]

Size of the file to allocate, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method fails if the file is read-only.

It is best to allocate as much space as possible—ideally, more than needed. However, this can result in a very large file that contains relatively little data. For example, a 1-gigabyte (GB) capture file might contain a few megabytes of captured video. Use the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-copycapturefile">ICaptureGraphBuilder2::CopyCaptureFile</a> method to copy the data into a new file. That method copies only the data and ignores the empty portion of the original file.

If you use this method to preallocate the file, call <a href="/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter2-setmode">IFileSinkFilter2::SetMode</a> on the file-writer filter with the value zero. If the filter is set to AM_FILE_OVERWRITE, it will delete the preallocated file. Note that some file-writer filters do not support mode 0.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>