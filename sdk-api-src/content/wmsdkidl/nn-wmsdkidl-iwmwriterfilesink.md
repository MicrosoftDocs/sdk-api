---
UID: NN:wmsdkidl.IWMWriterFileSink
title: IWMWriterFileSink (wmsdkidl.h)
author: windows-sdk-content
description: The IWMWriterFileSink interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the WMCreateWriterFileSink function.
old-location: wmformat\iwmwriterfilesink.htm
tech.root: wmformat
ms.assetid: af47b130-353e-411d-8432-09ecd20a70d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriterFileSink, IWMWriterFileSink interface [windows Media Format], IWMWriterFileSink interface [windows Media Format],described, IWMWriterFileSinkInterface, wmformat.iwmwriterfilesink, wmsdkidl/IWMWriterFileSink
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMWriterFileSink"
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
 - IWMWriterFileSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterFileSink interface


## -description



The <b>IWMWriterFileSink</b> interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink">WMCreateWriterFileSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterFileSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterFileSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open">Open</a>
</td>
<td align="left" width="63%">
Opens a file that acts as the writer sink.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2</a>
</td>
<td>IID_IWMWriterFileSink2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3</a>
</td>
<td>IID_IWMWriterFileSink3</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-file-sinks">Using File Sinks</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

