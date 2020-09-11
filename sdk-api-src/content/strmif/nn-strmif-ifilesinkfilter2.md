---
UID: NN:strmif.IFileSinkFilter2
title: IFileSinkFilter2 (strmif.h)
description: The IFileSinkFilter2 interface extends the IFileSinkFilter interface.
helpviewer_keywords: ["IFileSinkFilter2","IFileSinkFilter2 interface [DirectShow]","IFileSinkFilter2 interface [DirectShow]","described","IFileSinkFilter2Interface","dshow.ifilesinkfilter2","strmif/IFileSinkFilter2"]
old-location: dshow\ifilesinkfilter2.htm
tech.root: dshow
ms.assetid: 1339c441-2b10-461f-87f3-4835c1692740
ms.date: 12/05/2018
ms.keywords: IFileSinkFilter2, IFileSinkFilter2 interface [DirectShow], IFileSinkFilter2 interface [DirectShow],described, IFileSinkFilter2Interface, dshow.ifilesinkfilter2, strmif/IFileSinkFilter2
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
 - IFileSinkFilter2
 - strmif/IFileSinkFilter2
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
 - IFileSinkFilter2
---

# IFileSinkFilter2 interface


## -description

The <b>IFileSinkFilter2</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter</a> interface. Filters that write media streams to a file implement this interface. A file sink filter in a video capture filter graph, for instance, saves the output of the video compression filter to a file. Typically, the application running this filter graph should allow the user to enter the name of the file to which to save the data. This interface enables you to communicate this information. 

<b>IFileSinkFilter2</b> adds the option to determine whether the file it writes should destroy an existing file of the same name. In the video capture case, do not destroy a file you've already created, because preallocating file space takes valuable time. By default, the new file does not destroy the old one. Otherwise, destroy the original file to make sure the file you author doesn't contain garbage.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSinkFilter2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter</a>. <b>IFileSinkFilter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSinkFilter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter2-getmode">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves whether the file writer destroys the file when it creates the new one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter2-setmode">SetMode</a>
</td>
<td align="left" width="63%">
Determines whether the file writer destroys the file when it creates the new one.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>

