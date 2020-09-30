---
UID: NF:strmif.IAMCopyCaptureFileProgress.Progress
title: IAMCopyCaptureFileProgress::Progress (strmif.h)
description: The Progress method is called periodically by the ICaptureGraphBuilder2::CopyCaptureFile method while it copies the file.
helpviewer_keywords: ["IAMCopyCaptureFileProgress interface [DirectShow]","Progress method","IAMCopyCaptureFileProgress.Progress","IAMCopyCaptureFileProgress::Progress","IAMCopyCaptureFileProgressProgress","Progress","Progress method [DirectShow]","Progress method [DirectShow]","IAMCopyCaptureFileProgress interface","dshow.iamcopycapturefileprogress_progress","strmif/IAMCopyCaptureFileProgress::Progress"]
old-location: dshow\iamcopycapturefileprogress_progress.htm
tech.root: dshow
ms.assetid: 6908627e-51de-4206-bdb2-b3aaedf9478f
ms.date: 12/05/2018
ms.keywords: IAMCopyCaptureFileProgress interface [DirectShow],Progress method, IAMCopyCaptureFileProgress.Progress, IAMCopyCaptureFileProgress::Progress, IAMCopyCaptureFileProgressProgress, Progress, Progress method [DirectShow], Progress method [DirectShow],IAMCopyCaptureFileProgress interface, dshow.iamcopycapturefileprogress_progress, strmif/IAMCopyCaptureFileProgress::Progress
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
 - IAMCopyCaptureFileProgress::Progress
 - strmif/IAMCopyCaptureFileProgress::Progress
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
 - IAMCopyCaptureFileProgress.Progress
---

# IAMCopyCaptureFileProgress::Progress


## -description

The <code>Progress</code> method is called periodically by the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-copycapturefile">ICaptureGraphBuilder2::CopyCaptureFile</a> method while it copies the file.

## -parameters

### -param iProgress [in]

Specifies the percentage of the copy operation that has completed, as a value between 0 and 100.

## -returns

Returns S_OK or an <b>HRESULT</b> error code.

## -remarks

Applications typically use the value of <i>iProgress</i> to update a progress bar on the user interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcopycapturefileprogress">IAMCopyCaptureFileProgress Interface</a>