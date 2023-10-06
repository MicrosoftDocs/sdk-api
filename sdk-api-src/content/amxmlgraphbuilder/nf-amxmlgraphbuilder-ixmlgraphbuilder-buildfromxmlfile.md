---
UID: NF:amxmlgraphbuilder.IXMLGraphBuilder.BuildFromXMLFile
title: IXMLGraphBuilder::BuildFromXMLFile (amxmlgraphbuilder.h)
description: The BuildFromXMLFile method loads a filter graph from an XML file.
helpviewer_keywords: ["BuildFromXMLFile","BuildFromXMLFile method [DirectShow]","BuildFromXMLFile method [DirectShow]","IXMLGraphBuilder interface","IXMLGraphBuilder interface [DirectShow]","BuildFromXMLFile method","IXMLGraphBuilder.BuildFromXMLFile","IXMLGraphBuilder::BuildFromXMLFile","IXMLGraphBuilderBuildFromXMLFile","amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXMLFile","dshow.ixmlgraphbuilder_buildfromxmlfile"]
old-location: dshow\ixmlgraphbuilder_buildfromxmlfile.htm
tech.root: dshow
ms.assetid: 238a3077-0f04-44bb-a6ac-b532ef97c315
ms.date: 4/26/2023
ms.keywords: BuildFromXMLFile, BuildFromXMLFile method [DirectShow], BuildFromXMLFile method [DirectShow],IXMLGraphBuilder interface, IXMLGraphBuilder interface [DirectShow],BuildFromXMLFile method, IXMLGraphBuilder.BuildFromXMLFile, IXMLGraphBuilder::BuildFromXMLFile, IXMLGraphBuilderBuildFromXMLFile, amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXMLFile, dshow.ixmlgraphbuilder_buildfromxmlfile
req.header: amxmlgraphbuilder.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLGraphBuilder::BuildFromXMLFile
 - amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXMLFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amxmlgraphbuilder.h
api_name:
 - IXMLGraphBuilder.BuildFromXMLFile
---

# IXMLGraphBuilder::BuildFromXMLFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>BuildFromXMLFile</b> method loads a filter graph from an XML file.


<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div><div> </div>

## -parameters

### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface. To create the <a href="/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a>, call <b>CoCreateInstance</b>. Do not add any filters to the graph before calling this method.

### -param wszFileName [in]

Wide-character string that contains the full path name of an XML file. The XML file must contain the string returned by the <a href="/windows/desktop/api/amxmlgraphbuilder/nf-amxmlgraphbuilder-ixmlgraphbuilder-savetoxml">IXMLGraphBuilder::SaveToXML</a> method.

### -param wszBaseURL [in]

Reserved. Set to <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amxmlgraphbuilder/nn-amxmlgraphbuilder-ixmlgraphbuilder">IXMLGraphBuilder Interface</a>