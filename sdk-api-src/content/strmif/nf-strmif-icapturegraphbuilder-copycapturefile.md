---
UID: NF:strmif.ICaptureGraphBuilder.CopyCaptureFile
title: ICaptureGraphBuilder::CopyCaptureFile (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Copies the valid media data from the preallocated capture file.
helpviewer_keywords: ["CopyCaptureFile","CopyCaptureFile method [DirectShow]","CopyCaptureFile method [DirectShow]","ICaptureGraphBuilder interface","ICaptureGraphBuilder interface [DirectShow]","CopyCaptureFile method","ICaptureGraphBuilder.CopyCaptureFile","ICaptureGraphBuilder::CopyCaptureFile","ICaptureGraphBuilderCopyCaptureFile","dshow.icapturegraphbuilder_copycapturefile","strmif/ICaptureGraphBuilder::CopyCaptureFile"]
old-location: dshow\icapturegraphbuilder_copycapturefile.htm
tech.root: dshow
ms.assetid: 6eb4a3ed-6914-4839-ab1f-18510483ab49
ms.date: 4/26/2023
ms.keywords: CopyCaptureFile, CopyCaptureFile method [DirectShow], CopyCaptureFile method [DirectShow],ICaptureGraphBuilder interface, ICaptureGraphBuilder interface [DirectShow],CopyCaptureFile method, ICaptureGraphBuilder.CopyCaptureFile, ICaptureGraphBuilder::CopyCaptureFile, ICaptureGraphBuilderCopyCaptureFile, dshow.icapturegraphbuilder_copycapturefile, strmif/ICaptureGraphBuilder::CopyCaptureFile
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ICaptureGraphBuilder::CopyCaptureFile
 - strmif/ICaptureGraphBuilder::CopyCaptureFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.CopyCaptureFile
---

# ICaptureGraphBuilder::CopyCaptureFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Copies the valid media data from the preallocated capture file.

## -parameters

### -param lpwstrOld [in]

Pointer to a Unicode™ string containing the source file name.

### -param lpwstrNew [in]

Pointer to a Unicode string containing the destination file name. Valid data is copied to this file.

### -param fAllowEscAbort [in]

Value indicating whether pressing the ESC key will cancel the copy operation. <b>TRUE</b> indicates that it will; <b>FALSE</b> indicates that this method will ignore that keystroke.

### -param pCallback [in]

Optional pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-iamcopycapturefileprogress">IAMCopyCaptureFileProgress</a> show the progress (percentage complete) of the copy operation.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The new file will contain only valid data and therefore can be much shorter than the source file. Typically, you will always capture to the same huge preallocated file and use this method to copy the data you want to save from each capture to a new file.

If you specify <i>pCallback</i>, the <a href="/windows/desktop/api/strmif/nf-strmif-iamcopycapturefileprogress-progress">Progress</a> method on the <a href="/windows/desktop/api/strmif/nn-strmif-iamcopycapturefileprogress">IAMCopyCaptureFileProgress</a> interface will be called periodically with an integer between 0 and 100 representing the percentage complete.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>