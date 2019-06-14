---
UID: NN:strmif.IConfigAviMux
title: IConfigAviMux (strmif.h)
author: windows-sdk-content
description: The IConfigAviMux interface configures the AVI Mux filter.
old-location: dshow\iconfigavimux.htm
tech.root: DirectShow
ms.assetid: 4cc3cdeb-ebc5-46e1-8cc4-84b40e91323b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConfigAviMux, IConfigAviMux interface [DirectShow], IConfigAviMux interface [DirectShow],described, IConfigAviMuxInterface, dshow.iconfigavimux, strmif/IConfigAviMux
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
 - IConfigAviMux
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAviMux interface


## -description



The <code>IConfigAviMux</code> interface configures the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter. Applications can use this interface to set the master stream and to create an AVI 1.0 index.

<code>IConfigAviMux</code> provides backward compatibility with older Video for Windows (VFW) Audio-Video Interleaved (AVI) index formats (idx1) as well as extended AVI 2.0 index formats (indx) to allow for file sizes greater than 1 gigabyte (GB). Set and retrieve the compatibility indexes by using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iconfigavimux-setoutputcompatibilityindex">IConfigAviMux::SetOutputCompatibilityIndex</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iconfigavimux-getoutputcompatibilityindex">IConfigAviMux::GetOutputCompatibilityIndex</a> methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigAviMux</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigAviMux</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConfigAviMux</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfigavimux-getmasterstream">GetMasterStream</a>
</td>
<td align="left" width="63%">
Queries which stream will be used to synchronize the other streams in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iconfigavimux-getoutputcompatibilityindex">GetOutputCompatibilityIndex</a>
</td>
<td align="left" width="63%">
Retrieves the setting for the AVI index format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iconfigavimux-setmasterstream">SetMasterStream</a>
</td>
<td align="left" width="63%">
Specifies a stream that will be used to synchronize the other streams in the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-iconfigavimux-setoutputcompatibilityindex">SetOutputCompatibilityIndex</a>
</td>
<td align="left" width="63%">
Sets the AVI index format.

</td>
</tr>
</table> 

