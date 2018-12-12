---
UID: NN:wmsdkidl.IWMWriterFileSink2
title: IWMWriterFileSink2
author: windows-sdk-content
description: The IWMWriterFileSink2 interface provides extended management of a file sink.This interface can be obtained by calling the QueryInterface method of an IWMWriterFileSink interface.
old-location: wmformat\iwmwriterfilesink2.htm
tech.root: wmformat
ms.assetid: 229ae2a5-103a-4a33-b7ca-c9b2854c6741
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterFileSink2, IWMWriterFileSink2 interface [windows Media Format], IWMWriterFileSink2 interface [windows Media Format],described, IWMWriterFileSink2Interface, wmformat.iwmwriterfilesink2, wmsdkidl/IWMWriterFileSink2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IWMWriterFileSink2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink2 interface


## -description



The <b>IWMWriterFileSink2</b> interface provides extended management of a file sink.

This interface can be obtained by calling the <b>QueryInterface</b> method of an <b>IWMWriterFileSink</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd798742(v=VS.85).aspx">IWMWriterFileSink</a>. <b>IWMWriterFileSink2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterFileSink2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798744(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes the sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798745(v=VS.85).aspx">GetFileDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the portion of the file that has been written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798746(v=VS.85).aspx">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798747(v=VS.85).aspx">IsClosed</a>
</td>
<td align="left" width="63%">
Ascertains whether the file sink has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798748(v=VS.85).aspx">IsStopped</a>
</td>
<td align="left" width="63%">
Ascertains whether the file sink has stopped writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798749(v=VS.85).aspx">Start</a>
</td>
<td align="left" width="63%">
Starts recording at the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798750(v=VS.85).aspx">Stop</a>
</td>
<td align="left" width="63%">
Stops recording at the specified time.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd798742(v=VS.85).aspx">IWMWriterFileSink</a>
</td>
<td>IID_IWMWriterFileSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798751(v=VS.85).aspx">IWMWriterFileSink3</a>
</td>
<td>IID_IWMWriterFileSink3</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798742(v=VS.85).aspx">IWMWriterFileSink Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798751(v=VS.85).aspx">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/0cc4320a-c975-452d-bd1c-394d43bd4585">Using File Sinks</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

