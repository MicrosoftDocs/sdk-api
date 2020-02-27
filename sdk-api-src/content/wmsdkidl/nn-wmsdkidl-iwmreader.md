---
UID: NN:wmsdkidl.IWMReader
title: IWMReader (wmsdkidl.h)
description: The IWMReader interface is used to open, close, start, pause, resume, and unlock the WMReader object.
old-location: wmformat\iwmreader.htm
tech.root: wmformat
ms.assetid: e995b707-d388-4ec3-b3c8-b111628c13d7
ms.date: 12/05/2018
ms.keywords: IWMReader, IWMReader interface [windows Media Format], IWMReader interface [windows Media Format],described, IWMReaderInterface, wmformat.iwmreader, wmsdkidl/IWMReader
f1_keywords:
- wmsdkidl/IWMReader
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader interface


## -description



The <b>IWMReader</b> interface is used to open, close, start, pause, resume, and unlock the <b>WMReader</b> object. It is also used to stop reading files, and to get and set the output properties.

Many of the methods in this interface are asynchronous and send status notifications to the application through an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method implemented in the application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-close">Close</a>
</td>
<td align="left" width="63%">
Deletes all outputs on the reader and releases the file resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of uncompressed media streams sent from the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat">GetOutputFormat</a>
</td>
<td align="left" width="63%">
Retrieves the supported formats for a specified output media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount">GetOutputFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of format types supported by this output media stream on the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">GetOutputProps</a>
</td>
<td align="left" width="63%">
Retrieves the current properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">Open</a>
</td>
<td align="left" width="63%">
Opens an ASF file for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the current read operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-resume">Resume</a>
</td>
<td align="left" width="63%">
Restarts read operation from the current time offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">SetOutputProps</a>
</td>
<td align="left" width="63%">
Specifies the properties of an uncompressed output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">Start</a>
</td>
<td align="left" width="63%">
Starts reading from the current time offset. Uncompressed data is passed to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops reading, after which there is no current read position.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
 

 

