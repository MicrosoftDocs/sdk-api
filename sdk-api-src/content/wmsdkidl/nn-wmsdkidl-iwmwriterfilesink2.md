---
UID: NN:wmsdkidl.IWMWriterFileSink2
title: IWMWriterFileSink2
author: windows-driver-content
description: The IWMWriterFileSink2 interface provides extended management of a file sink.This interface can be obtained by calling the QueryInterface method of an IWMWriterFileSink interface.
old-location: wmformat\iwmwriterfilesink2.htm
old-project: wmformat
ms.assetid: 229ae2a5-103a-4a33-b7ca-c9b2854c6741
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMWriterFileSink2, IWMWriterFileSink2 interface [windows Media Format], IWMWriterFileSink2 interface [windows Media Format], described, IWMWriterFileSink2Interface, wmformat.iwmwriterfilesink2, wmsdkidl/IWMWriterFileSink2
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMWriterFileSink2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink2 interface


## -description



The <b>IWMWriterFileSink2</b> interface provides extended management of a file sink.

This interface can be obtained by calling the <b>QueryInterface</b> method of an <b>IWMWriterFileSink</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink2</b> interface inherits from <a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink</a>. <b>IWMWriterFileSink2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0685760-929d-4c65-84e0-a9745635eddd">GetFileDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the portion of the file that has been written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a5f0c18-f73a-461e-b3cf-48742e74fed3">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ae9137f-ce43-4860-a28f-deac39f216a4">IsClosed</a>
</td>
<td align="left" width="63%">
Ascertains whether the file sink has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1e5790a-3cac-4e0e-8a3f-b21afe2711ff">IsStopped</a>
</td>
<td align="left" width="63%">
Ascertains whether the file sink has stopped writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts recording at the specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
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
<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink</a>
</td>
<td>IID_IWMWriterFileSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3</a>
</td>
<td>IID_IWMWriterFileSink3</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink Interface</a>



<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/0cc4320a-c975-452d-bd1c-394d43bd4585">Using File Sinks</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

