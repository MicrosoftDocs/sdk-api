---
UID: NN:wmsdkidl.IWMWriterFileSink3
title: IWMWriterFileSink3
author: windows-sdk-content
description: The IWMWriterFileSink3 interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call QueryInterface on the file sink object.
old-location: wmformat\iwmwriterfilesink3.htm
tech.root: wmformat
ms.assetid: 67f418c8-184d-46f0-8939-69194c7e7a50
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMWriterFileSink3, IWMWriterFileSink3 interface [windows Media Format], IWMWriterFileSink3 interface [windows Media Format],described, IWMWriterFileSink3Interface, wmformat.iwmwriterfilesink3, wmsdkidl/IWMWriterFileSink3
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMWriterFileSink3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink3 interface


## -description



The <b>IWMWriterFileSink3</b> interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the file sink object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterFileSink3</b> interface inherits from <a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2</a>. <b>IWMWriterFileSink3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6eb4f09f-627e-4409-9f08-8f655aa7d0ec">CompleteOperations</a>
</td>
<td align="left" width="63%">
Stops writing after completing all operations in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6412ce4-03ac-4777-8eb2-ef9f265a6d6c">GetAutoIndexing</a>
</td>
<td align="left" width="63%">
Ascertains whether automatic indexing is set for the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8a7003e-e59f-451c-9f45-75d6d094a03b">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the supported file sink mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e87222eb-6ed1-49b7-a544-27703ba9806b">GetUnbufferedIO</a>
</td>
<td align="left" width="63%">
Ascertains whether unbuffered I/O is used for the file sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dbcb27b-7588-4475-99fe-3e547d1659d3">OnDataUnitEx</a>
</td>
<td align="left" width="63%">
Retrieves information about data units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c8f1c25-d752-42b6-87b7-9d6a6e38642f">SetAutoIndexing</a>
</td>
<td align="left" width="63%">
Enables or disables automatic indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c103d205-a568-4206-a66e-5473e16cfa3f">SetControlStream</a>
</td>
<td align="left" width="63%">
Sets a stream as a control stream or removes control from a control stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a9c21b-d301-41e4-a9bc-321a5b2decca">SetUnbufferedIO</a>
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
<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink</a>
</td>
<td>IID_IWMWriterFileSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2</a>
</td>
<td>IID_IWMWriterFileSink2</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink Interface</a>



<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>



<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink Interface</a>



<a href="https://msdn.microsoft.com/0cc4320a-c975-452d-bd1c-394d43bd4585">Using File Sinks</a>



<a href="https://msdn.microsoft.com/93f44579-fb2d-498e-a271-5bc91d6f0321">Writer File Sink Object</a>
 

 

