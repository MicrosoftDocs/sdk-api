---
UID: NN:qnetwork.IAMNetShowExProps
title: IAMNetShowExProps
author: windows-sdk-content
description: The IAMNetShowExProps interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
old-location: dshow\iamnetshowexprops.htm
old-project: DirectShow
ms.assetid: e68959dc-1a79-4e2c-aeaf-3febcb9c09ce
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMNetShowExProps, IAMNetShowExProps interface [DirectShow], IAMNetShowExProps interface [DirectShow],described, IAMNetShowExPropsInterface, dshow.iamnetshowexprops, qnetwork/IAMNetShowExProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: qnetwork.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMNetShowExProps interface


## -description



The <code>IAMNetShowExProps</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowExProps</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAMNetShowExProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMNetShowExProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/042ddea5-c17a-4cd6-a18d-9a3b65bf11b7">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b16727d-565a-431e-8124-124d72816d65">get_CodecCount</a>
</td>
<td align="left" width="63%">
Retrieves the number codecs needed to play the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a9cbaed-c8aa-445a-9f8e-d84a7b50166e">get_CreationDate</a>
</td>
<td align="left" width="63%">
Retrieves the creation date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab731d68-969b-425d-978a-879b15c06a88">get_ErrorCorrection</a>
</td>
<td align="left" width="63%">
Retrieves the error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d79169-ae1b-4532-b367-ec2d24fae0b1">get_SourceLink</a>
</td>
<td align="left" width="63%">
Retrieves the source link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/498e81fc-90d3-4a24-b672-c7c62b3bfd39">get_SourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a26e576-df4a-462d-8fab-0a133469e77b">GetCodecDescription</a>
</td>
<td align="left" width="63%">
Retrieves the user-friendly description of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/597178a5-8ead-4562-adbe-e6cd2b352d25">GetCodecInstalled</a>
</td>
<td align="left" width="63%">
Queries whether a specified codec is installed on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad5672a8-2af9-45ef-b510-3c2f8948f64b">GetCodecURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which the codec may be downloaded.

</td>
</tr>
</table> 


## -remarks



To define the interface identifier, include the header file Initguid.h before Qnetwork.h, but after Dshow.h and other header files:

<pre class="syntax" xml:space="preserve"><code>#include &lt;dshow.h&gt;
#include &lt;initguid.h&gt;
#include &lt;qnetwork.h&gt;
</code></pre>
<div class="alert"><b>Note</b>  Make sure that Initguid.h is included only once in your project. Otherwise, you will receive linker errors for duplicate GUID values.</div>
<div> </div>



## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

