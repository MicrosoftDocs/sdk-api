---
UID: NN:strmif.IFileSinkFilter
title: IFileSinkFilter (strmif.h)
description: The IFileSinkFilter interface is implemented on filters that write media streams to a file.helpviewer_keywords: ["IFileSinkFilter","IFileSinkFilter interface [DirectShow]","IFileSinkFilter interface [DirectShow]","described","IFileSinkFilterInterface","dshow.ifilesinkfilter","strmif/IFileSinkFilter"]
old-location: dshow\ifilesinkfilter.htm
tech.root: DirectShow
ms.assetid: aa1d3f8e-9790-4442-ba7e-896981bf1b96
ms.date: 12/05/2018
ms.keywords: IFileSinkFilter, IFileSinkFilter interface [DirectShow], IFileSinkFilter interface [DirectShow],described, IFileSinkFilterInterface, dshow.ifilesinkfilter, strmif/IFileSinkFilter
f1_keywords:
- strmif/IFileSinkFilter
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
- IFileSinkFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSinkFilter interface


## -description



The <code>IFileSinkFilter</code> interface is implemented on filters that write media streams to a file. A file sink filter in a video capture filter graph, for instance, writes the output of the video compression filter to a file. Typically, the application running this filter graph should enable the user to enter the name of the file to be written to. This interface enables the communication of this information.

If a filter needs the name of an output file, it should expose this interface to allow an application to set the file name. Note that there is currently no base class implementation of this interface.

Any application that must set the name of the file into which the file sink filter will write should use this interface to get and set the file name.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSinkFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSinkFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSinkFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter-getcurfile">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current file into which media samples will be written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter-setfilename">SetFileName</a>
</td>
<td align="left" width="63%">
Sets the name of the file into which media samples will be written.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter2">IFileSinkFilter2</a> interface extends <b>IFileSinkFilter</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

