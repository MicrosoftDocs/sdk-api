---
UID: NN:wmsdkidl.IWMReaderAdvanced2
title: IWMReaderAdvanced2 (wmsdkidl.h)
description: The IWMReaderAdvanced2 interface provides additional advanced methods for a reader object.
helpviewer_keywords: ["IWMReaderAdvanced2","IWMReaderAdvanced2 interface [windows Media Format]","IWMReaderAdvanced2 interface [windows Media Format]","described","IWMReaderAdvanced2Interface","wmformat.iwmreaderadvanced2","wmsdkidl/IWMReaderAdvanced2"]
old-location: wmformat\iwmreaderadvanced2.htm
tech.root: wmformat
ms.assetid: 5d741e49-9fdf-4f8d-9ea1-faaecf879be4
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced2, IWMReaderAdvanced2 interface [windows Media Format], IWMReaderAdvanced2 interface [windows Media Format],described, IWMReaderAdvanced2Interface, wmformat.iwmreaderadvanced2, wmsdkidl/IWMReaderAdvanced2
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMReaderAdvanced2
 - wmsdkidl/IWMReaderAdvanced2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMReaderAdvanced2
---

# IWMReaderAdvanced2 interface


## -description

The <b>IWMReaderAdvanced2</b> interface provides additional advanced methods for a reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAdvanced2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced</a>. <b>IWMReaderAdvanced2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAdvanced2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress">GetBufferProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been buffered, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress">GetDownloadProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getlogclientid">GetLogClientID</a>
</td>
<td align="left" width="63%">
Queries whether the reader logs the client's unique ID or an anonymous session ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting">GetOutputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular output by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode">GetPlayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname">GetProtocolName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the protocol that is currently being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getsaveasprogress">GetSaveAsProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of data that has been saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream">OpenStream</a>
</td>
<td align="left" width="63%">
Opens a Windows Media stream for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-preroll">Preroll</a>
</td>
<td align="left" width="63%">
Begins prerolling the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas">SaveFileAs</a>
</td>
<td align="left" width="63%">
Saves the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid">SetLogClientID</a>
</td>
<td align="left" width="63%">
Specifies whether the reader logs the client's unique ID or an anonymous session ID..

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting">SetOutputSetting</a>
</td>
<td align="left" width="63%">
Specifies a named setting for a particular output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode">SetPlayMode</a>
</td>
<td align="left" width="63%">
Specifies the current play mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker">StartAtMarker</a>
</td>
<td align="left" width="63%">
Starts the reader from a specified <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">marker</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-stopbuffering">StopBuffering</a>
</td>
<td align="left" width="63%">
Requests that the reader stops buffering as soon as possible.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>

