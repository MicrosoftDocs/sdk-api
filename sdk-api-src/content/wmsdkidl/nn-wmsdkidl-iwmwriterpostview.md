---
UID: NN:wmsdkidl.IWMWriterPostView
title: IWMWriterPostView
author: windows-driver-content
description: The IWMWriterPostView interface manages advanced writing functionality related to the postviewing of samples.
old-location: wmformat\iwmwriterpostview.htm
old-project: wmformat
ms.assetid: 1d24dbd6-86df-4a0a-8110-15f6a4c1f31d
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMWriterPostView, IWMWriterPostView interface [windows Media Format], IWMWriterPostView interface [windows Media Format], described, IWMWriterPostViewInterface, wmformat.iwmwriterpostview, wmsdkidl/IWMWriterPostView
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
-	IWMWriterPostView
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/bd17eeec-a1ce-42db-a807-008ca2c4194f">GetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Ascertains whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3636833d-3c96-45d9-bf82-e3ff930c7d9b">GetPostViewFormat</a>
</td>
<td align="left" width="63%">
Retrieves the media properties for the specified output stream and output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b34b2418-5ae4-49a2-913a-bb4ac604ac4e">GetPostViewFormatCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of possible output formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39dc32d1-53e5-43b5-bc96-074dc286890e">GetPostViewProps</a>
</td>
<td align="left" width="63%">
Retrieves the properties for the specified output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93120e68-2d1c-4628-8e2e-d22a56fa98a3">GetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Ascertains whether delivery of postview samples is enabled for the specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/995bf3fa-3e10-46a2-ad51-55375d6af447">SetAllocateForPostView</a>
</td>
<td align="left" width="63%">
Specifies whether the application, and not the writer, must supply the buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2814f32-1787-44a6-8ffc-5d2a9aca8601">SetPostViewCallback</a>
</td>
<td align="left" width="63%">
Specifies the callback interface to use for receiving postview samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5b92065-fff3-41d2-b263-375ae14869e5">SetPostViewProps</a>
</td>
<td align="left" width="63%">
Specifies the properties for the output stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d58671a-357b-412b-ad77-61866b0dcce3">SetReceivePostViewSamples</a>
</td>
<td align="left" width="63%">
Enables or disables delivery of postview samples for the specified stream.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/987dd3b4-2245-4640-820c-5a9660ab5e37">IWMWriterPostViewCallback Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/9da3c749-f6bd-43b5-9eff-3a637ddef048">To Use Writer Postview</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

