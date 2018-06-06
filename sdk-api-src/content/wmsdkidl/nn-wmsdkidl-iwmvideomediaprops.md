---
UID: NN:wmsdkidl.IWMVideoMediaProps
title: IWMVideoMediaProps
author: windows-sdk-content
description: With this interface, the application can specify additional video-specific parameters not available on the IWMMediaProps interface.To get access to the methods of this interface, call QueryInterface on a stream configuration object.
old-location: wmformat\iwmvideomediaprops.htm
old-project: wmformat
ms.assetid: 4d6ba1d8-b046-450b-a3f9-4810faba5b77
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMVideoMediaProps, IWMVideoMediaProps interface [windows Media Format], IWMVideoMediaProps interface [windows Media Format],described, IWMVideoMediaPropsInterface, wmformat.iwmvideomediaprops, wmsdkidl/IWMVideoMediaProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
api_name:
 - IWMVideoMediaProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMVideoMediaProps interface


## -description



With this interface, the application can specify additional video-specific parameters not available on the <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a> interface.

To get access to the methods of this interface, call <b>QueryInterface</b> on a stream configuration object. For more information, see <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMVideoMediaProps</b> interface inherits from <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>. <b>IWMVideoMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMVideoMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/125d352e-b181-4baa-8763-21315534beea">GetMaxKeyFrameSpacing</a>
</td>
<td align="left" width="63%">
Retrieves the maximum interval between key frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9edfe229-ffc5-4266-93af-1938bbd577c2">GetQuality</a>
</td>
<td align="left" width="63%">
Retrieves the quality setting for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d1a9090-2658-45bd-8893-30e063d10aa8">SetMaxKeyFrameSpacing</a>
</td>
<td align="left" width="63%">
Specifies the maximum interval between key frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f91380d-b8c8-47db-99ca-12c897bdff20">SetQuality</a>
</td>
<td align="left" width="63%">
Specifies the quality setting for the video stream.

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
<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>
</td>
<td>IID_IWMMediaProps</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0e51a9be-afd4-430b-8339-f45e8f9a7d20">IWMPropertyVault</a>
</td>
<td>IID_IWMPropertyVault</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a>
</td>
<td>IID_IWMStreamConfig</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681">IWMStreamConfig3</a>
</td>
<td>IID_IWMStreamConfig3</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

