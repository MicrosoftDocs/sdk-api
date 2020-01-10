---
UID: NN:wmsdkidl.IWMWriterFileSink3
title: IWMWriterFileSink3 (wmsdkidl.h)
description: The IWMWriterFileSink3 interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call QueryInterface on the file sink object.
old-location: wmformat\iwmwriterfilesink3.htm
tech.root: wmformat
ms.assetid: 67f418c8-184d-46f0-8939-69194c7e7a50
ms.date: 12/05/2018
ms.keywords: IWMWriterFileSink3, IWMWriterFileSink3 interface [windows Media Format], IWMWriterFileSink3 interface [windows Media Format],described, IWMWriterFileSink3Interface, wmformat.iwmwriterfilesink3, wmsdkidl/IWMWriterFileSink3
f1_keywords:
- wmsdkidl/IWMWriterFileSink3
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
- IWMWriterFileSink3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterFileSink3 interface


## -description



The <b>IWMWriterFileSink3</b> interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the file sink object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2</a>. <b>IWMWriterFileSink3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterFileSink3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-completeoperations">CompleteOperations</a>
</td>
<td align="left" width="63%">
Stops writing after completing all operations in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing">GetAutoIndexing</a>
</td>
<td align="left" width="63%">
Ascertains whether automatic indexing is set for the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getmode">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the supported file sink mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getunbufferedio">GetUnbufferedIO</a>
</td>
<td align="left" width="63%">
Ascertains whether unbuffered I/O is used for the file sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-ondataunitex">OnDataUnitEx</a>
</td>
<td align="left" width="63%">
Retrieves information about data units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing">SetAutoIndexing</a>
</td>
<td align="left" width="63%">
Enables or disables automatic indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setcontrolstream">SetControlStream</a>
</td>
<td align="left" width="63%">
Sets a stream as a control stream or removes control from a control stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setunbufferedio">SetUnbufferedIO</a>
</td>
<td align="left" width="63%">
Specifies whether unbuffered I/O is used for the file sink.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink</a>
</td>
<td>IID_IWMWriterFileSink</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2</a>
</td>
<td>IID_IWMWriterFileSink2</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-file-sinks">Using File Sinks</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-file-sink-object">Writer File Sink Object</a>
 

 

