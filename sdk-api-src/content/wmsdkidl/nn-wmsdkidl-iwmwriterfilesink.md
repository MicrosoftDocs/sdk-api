---
UID: NN:wmsdkidl.IWMWriterFileSink
title: IWMWriterFileSink
author: windows-driver-content
description: The IWMWriterFileSink interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the WMCreateWriterFileSink function.
old-location: wmformat\iwmwriterfilesink.htm
old-project: wmformat
ms.assetid: af47b130-353e-411d-8432-09ecd20a70d2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMWriterFileSink, IWMWriterFileSink interface [windows Media Format], IWMWriterFileSink interface [windows Media Format],described, IWMWriterFileSinkInterface, wmformat.iwmwriterfilesink, wmsdkidl/IWMWriterFileSink
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
-	IWMWriterFileSink
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink interface


## -description



The <b>IWMWriterFileSink</b> interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the <a href="https://msdn.microsoft.com/aeeaf67c-119f-482b-b064-87739499abda">WMCreateWriterFileSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink</b> interface inherits from <a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>. <b>IWMWriterFileSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
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
<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2</a>
</td>
<td>IID_IWMWriterFileSink2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3</a>
</td>
<td>IID_IWMWriterFileSink3</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>



<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/0cc4320a-c975-452d-bd1c-394d43bd4585">Using File Sinks</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

