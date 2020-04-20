---
UID: NN:strmif.IFileSourceFilter
title: IFileSourceFilter (strmif.h)
description: The IFileSourceFilter interface is exposed by source filters to set the file name and media type of the media file that they are to render.helpviewer_keywords: ["IFileSourceFilter","IFileSourceFilter interface [DirectShow]","IFileSourceFilter interface [DirectShow]","described","IFileSourceFilterInterface","dshow.ifilesourcefilter","strmif/IFileSourceFilter"]
old-location: dshow\ifilesourcefilter.htm
tech.root: DirectShow
ms.assetid: ad70fddb-4fc9-4010-a469-9a8ca4b47379
ms.date: 12/05/2018
ms.keywords: IFileSourceFilter, IFileSourceFilter interface [DirectShow], IFileSourceFilter interface [DirectShow],described, IFileSourceFilterInterface, dshow.ifilesourcefilter, strmif/IFileSourceFilter
f1_keywords:
- strmif/IFileSourceFilter
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IFileSourceFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSourceFilter interface


## -description



The <code>IFileSourceFilter</code> interface is exposed by source filters to set the file name and media type of the media file that they are to render. It is an abbreviated version of the COM <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> interface. If the file has a type that can be determined by the algorithm described in <a href="https://docs.microsoft.com/windows/desktop/DirectShow/registering-a-custom-file-type">Registering a Custom File Type</a>, the recommended file source filter CLSID is used when the filter graph manager attempts to render the filter graph.

If a filter needs the name of a file to open, it should expose this interface to allow an application to set the file name. Note that there is no base class implementation of this interface.

An application that inserts file source filters directly must query for this interface and set the file name. Normally, the filter graph manager uses this interface when an application calls <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>. The Graphedt.exe tool queries for the <b>IFileSourceFilter</b> interface and prompts for a file name if it finds it.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSourceFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSourceFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSourceFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesourcefilter-getcurfile">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesourcefilter-load">Load</a>
</td>
<td align="left" width="63%">
Loads the source filter with the file.

</td>
</tr>
</table> 

