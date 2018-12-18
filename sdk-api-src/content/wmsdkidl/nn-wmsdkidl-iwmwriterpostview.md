---
UID: NN:wmsdkidl.IWMWriterPostView
title: IWMWriterPostView
author: windows-sdk-content
description: The IWMWriterPostView interface manages advanced writing functionality related to the postviewing of samples.
old-location: wmformat\iwmwriterpostview.htm
tech.root: wmformat
ms.assetid: 1d24dbd6-86df-4a0a-8110-15f6a4c1f31d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterPostView, IWMWriterPostView interface [windows Media Format], IWMWriterPostView interface [windows Media Format],described, IWMWriterPostViewInterface, wmformat.iwmwriterpostview, wmsdkidl/IWMWriterPostView
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
 - IWMWriterPostView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPostView interface


## -description



The <b>IWMWriterPostView</b> interface manages advanced writing functionality related to the postviewing of samples. Postviewing displays the media samples as a viewer of the ASF file would see them, and is often used after encoding to check the output. Postviewing is supported only for video.

This interface can be obtained from any interface on the writer object by calling <b>QueryInterface</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPostView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMWriterPostView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPostView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798774(v=VS.85).aspx">GetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Ascertains whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798775(v=VS.85).aspx">GetPostViewFormat</a>
</td>
<td align="left" width="63%">
Retrieves the media properties for the specified output stream and output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798776(v=VS.85).aspx">GetPostViewFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of possible output formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798778(v=VS.85).aspx">GetPostViewProps</a>
</td>
<td align="left" width="63%">
Retrieves the properties for the specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798779(v=VS.85).aspx">GetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether delivery of postview samples is enabled for the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798780(v=VS.85).aspx">SetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Specifies whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798781(v=VS.85).aspx">SetPostViewCallback</a>
</td>
<td align="left" width="63%">
Specifies the callback interface to use for receiving postview samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798782(v=VS.85).aspx">SetPostViewProps</a>
</td>
<td align="left" width="63%">
Specifies the properties for the output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798783(v=VS.85).aspx">SetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Enables or disables delivery of postview samples for the specified stream.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798771(v=VS.85).aspx">IWMWriterPostViewCallback Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/9da3c749-f6bd-43b5-9eff-3a637ddef048">To Use Writer Postview</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

