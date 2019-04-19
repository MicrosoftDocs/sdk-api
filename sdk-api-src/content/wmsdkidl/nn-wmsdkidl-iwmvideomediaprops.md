---
UID: NN:wmsdkidl.IWMVideoMediaProps
title: IWMVideoMediaProps (wmsdkidl.h)
author: windows-sdk-content
description: With this interface, the application can specify additional video-specific parameters not available on the IWMMediaProps interface.To get access to the methods of this interface, call QueryInterface on a stream configuration object.
old-location: wmformat\iwmvideomediaprops.htm
tech.root: wmformat
ms.assetid: 4d6ba1d8-b046-450b-a3f9-4810faba5b77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMVideoMediaProps, IWMVideoMediaProps interface [windows Media Format], IWMVideoMediaProps interface [windows Media Format],described, IWMVideoMediaPropsInterface, wmformat.iwmvideomediaprops, wmsdkidl/IWMVideoMediaProps
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
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMVideoMediaProps interface


## -description



With this interface, the application can specify additional video-specific parameters not available on the <a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps</a> interface.

To get access to the methods of this interface, call <b>QueryInterface</b> on a stream configuration object. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig Interface</a>).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMVideoMediaProps</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps</a>. <b>IWMVideoMediaProps</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798712(v=VS.85).aspx">GetMaxKeyFrameSpacing</a>
</td>
<td align="left" width="63%">
Retrieves the maximum interval between key frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798713(v=VS.85).aspx">GetQuality</a>
</td>
<td align="left" width="63%">
Retrieves the quality setting for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798714(v=VS.85).aspx">SetMaxKeyFrameSpacing</a>
</td>
<td align="left" width="63%">
Specifies the maximum interval between key frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798715(v=VS.85).aspx">SetQuality</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps</a>
</td>
<td>IID_IWMMediaProps</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757416(v=VS.85).aspx">IWMPropertyVault</a>
</td>
<td>IID_IWMPropertyVault</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig</a>
</td>
<td>IID_IWMStreamConfig</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798547(v=VS.85).aspx">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798554(v=VS.85).aspx">IWMStreamConfig3</a>
</td>
<td>IID_IWMStreamConfig3</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

