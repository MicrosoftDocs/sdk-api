---
UID: NF:strmif.IGraphBuilder.SetLogFile
title: IGraphBuilder::SetLogFile (strmif.h)
description: The SetLogFile method sets the file for logging actions taken when attempting to perform an operation.
helpviewer_keywords: ["IGraphBuilder interface [DirectShow]","SetLogFile method","IGraphBuilder.SetLogFile","IGraphBuilder::SetLogFile","IGraphBuilderSetLogFile","SetLogFile","SetLogFile method [DirectShow]","SetLogFile method [DirectShow]","IGraphBuilder interface","dshow.igraphbuilder_setlogfile","strmif/IGraphBuilder::SetLogFile"]
old-location: dshow\igraphbuilder_setlogfile.htm
tech.root: dshow
ms.assetid: 194960ee-3418-420f-9242-a372097e4dc9
ms.date: 4/26/2023
ms.keywords: IGraphBuilder interface [DirectShow],SetLogFile method, IGraphBuilder.SetLogFile, IGraphBuilder::SetLogFile, IGraphBuilderSetLogFile, SetLogFile, SetLogFile method [DirectShow], SetLogFile method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_setlogfile, strmif/IGraphBuilder::SetLogFile
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
 - IGraphBuilder::SetLogFile
 - strmif/IGraphBuilder::SetLogFile
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
 - IGraphBuilder.SetLogFile
---

# IGraphBuilder::SetLogFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetLogFile</code> method sets the file for logging actions taken when attempting to perform an operation.

## -parameters

### -param hFile

Handle to the log file.

## -returns

Returns S_OK.

## -remarks

This method is for use in debugging; it is intended to help you determine the cause of any failure to automatically build a filter graph.

The <i>hFile</i> parameter must be an open file handle. Your application is responsible for opening the file and for closing it when you are done logging. Before closing the file handle, call <code>SetLogFile</code> with a <b>NULL</b> file handle. This will ensure that the component does not attempt to use the file handle after you have closed it.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>