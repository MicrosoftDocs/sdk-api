---
UID: NF:amxmlgraphbuilder.IXMLGraphBuilder.BuildFromXML
title: IXMLGraphBuilder::BuildFromXML (amxmlgraphbuilder.h)
description: The BuildFromXML method loads a filter graph from an XML element.
helpviewer_keywords: ["BuildFromXML","BuildFromXML method [DirectShow]","BuildFromXML method [DirectShow]","IXMLGraphBuilder interface","IXMLGraphBuilder interface [DirectShow]","BuildFromXML method","IXMLGraphBuilder.BuildFromXML","IXMLGraphBuilder::BuildFromXML","IXMLGraphBuilderBuildFromXML","amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXML","dshow.ixmlgraphbuilder_buildfromxml"]
old-location: dshow\ixmlgraphbuilder_buildfromxml.htm
tech.root: dshow
ms.assetid: 953449da-620e-44cd-880c-b4c13d8bdbf6
ms.date: 4/26/2023
ms.keywords: BuildFromXML, BuildFromXML method [DirectShow], BuildFromXML method [DirectShow],IXMLGraphBuilder interface, IXMLGraphBuilder interface [DirectShow],BuildFromXML method, IXMLGraphBuilder.BuildFromXML, IXMLGraphBuilder::BuildFromXML, IXMLGraphBuilderBuildFromXML, amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXML, dshow.ixmlgraphbuilder_buildfromxml
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
 - IXMLGraphBuilder::BuildFromXML
 - amxmlgraphbuilder/IXMLGraphBuilder::BuildFromXML
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
 - IXMLGraphBuilder.BuildFromXML
---

# IXMLGraphBuilder::BuildFromXML


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>BuildFromXML</b> method loads a filter graph from an XML element.


<div class="alert"><b>Note</b>  Support for this interface was removed in Windows 7. New applications should not use this interface.</div><div> </div>

## -parameters

### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface. To create the <a href="/windows/desktop/DirectShow/filter-graph-manager">Filter Graph Manager</a>, call <b>CoCreateInstance</b>. Do not add any filters to the graph before calling this method.

### -param pxml [in]

Pointer to the <b>IXMLElement</b> interface of an XML element object. The XML element object must contain the string returned by the <a href="/windows/desktop/api/amxmlgraphbuilder/nf-amxmlgraphbuilder-ixmlgraphbuilder-savetoxml">IXMLGraphBuilder::SaveToXML</a> method.

<div class="alert"><b>Note</b>  The <b>IXMLElement</b> interface is implemented in Microsoft XML Core Services (MSXML) version 1.0 but is not implemented in more recent versions of MSXML.</div>
<div> </div>

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amxmlgraphbuilder/nn-amxmlgraphbuilder-ixmlgraphbuilder">IXMLGraphBuilder Interface</a>