---
UID: NN:strmif.IFileSourceFilter
title: IFileSourceFilter
author: windows-sdk-content
description: The IFileSourceFilter interface is exposed by source filters to set the file name and media type of the media file that they are to render.
old-location: dshow\ifilesourcefilter.htm
tech.root: DirectShow
ms.assetid: ad70fddb-4fc9-4010-a469-9a8ca4b47379
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFileSourceFilter, IFileSourceFilter interface [DirectShow], IFileSourceFilter interface [DirectShow],described, IFileSourceFilterInterface, dshow.ifilesourcefilter, strmif/IFileSourceFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSourceFilter interface


## -description



The <code>IFileSourceFilter</code> interface is exposed by source filters to set the file name and media type of the media file that they are to render. It is an abbreviated version of the COM <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> interface. If the file has a type that can be determined by the algorithm described in <a href="https://msdn.microsoft.com/bc0d5719-6325-40fe-8261-ad00b91f272c">Registering a Custom File Type</a>, the recommended file source filter CLSID is used when the filter graph manager attempts to render the filter graph.

If a filter needs the name of a file to open, it should expose this interface to allow an application to set the file name. Note that there is no base class implementation of this interface.

An application that inserts file source filters directly must query for this interface and set the file name. Normally, the filter graph manager uses this interface when an application calls <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>. The Graphedt.exe tool queries for the <b>IFileSourceFilter</b> interface and prompts for a file name if it finds it.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSourceFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileSourceFilter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/67373df9-06a3-4678-b661-29580df4f359">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a44b8153-19d5-43ad-936c-214c694eeeb6">Load</a>
</td>
<td align="left" width="63%">
Loads the source filter with the file.

</td>
</tr>
</table> 

