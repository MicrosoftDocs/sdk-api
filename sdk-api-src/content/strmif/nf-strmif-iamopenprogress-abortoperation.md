---
UID: NF:strmif.IAMOpenProgress.AbortOperation
title: IAMOpenProgress::AbortOperation (strmif.h)
description: The AbortOperation method cancels the file-open operation.
helpviewer_keywords: ["AbortOperation","AbortOperation method [DirectShow]","AbortOperation method [DirectShow]","IAMOpenProgress interface","IAMOpenProgress interface [DirectShow]","AbortOperation method","IAMOpenProgress.AbortOperation","IAMOpenProgress::AbortOperation","IAMOpenProgressAbortOperation","dshow.iamopenprogress_abortoperation","strmif/IAMOpenProgress::AbortOperation"]
old-location: dshow\iamopenprogress_abortoperation.htm
tech.root: dshow
ms.assetid: 5c20b57c-c491-4465-9626-13335191b5bb
ms.date: 4/26/2023
ms.keywords: AbortOperation, AbortOperation method [DirectShow], AbortOperation method [DirectShow],IAMOpenProgress interface, IAMOpenProgress interface [DirectShow],AbortOperation method, IAMOpenProgress.AbortOperation, IAMOpenProgress::AbortOperation, IAMOpenProgressAbortOperation, dshow.iamopenprogress_abortoperation, strmif/IAMOpenProgress::AbortOperation
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
 - IAMOpenProgress::AbortOperation
 - strmif/IAMOpenProgress::AbortOperation
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
 - IAMOpenProgress.AbortOperation
---

# IAMOpenProgress::AbortOperation


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AbortOperation</code> method cancels the file-open operation.



## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamopenprogress">IAMOpenProgress Interface</a>
