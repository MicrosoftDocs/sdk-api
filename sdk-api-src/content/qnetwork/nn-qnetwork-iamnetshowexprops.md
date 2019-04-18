---
UID: NN:qnetwork.IAMNetShowExProps
title: IAMNetShowExProps (qnetwork.h)
author: windows-sdk-content
description: The IAMNetShowExProps interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
old-location: dshow\iamnetshowexprops.htm
tech.root: DirectShow
ms.assetid: e68959dc-1a79-4e2c-aeaf-3febcb9c09ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMNetShowExProps, IAMNetShowExProps interface [DirectShow], IAMNetShowExProps interface [DirectShow],described, IAMNetShowExPropsInterface, dshow.iamnetshowexprops, qnetwork/IAMNetShowExProps
ms.topic: interface
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowExProps interface


## -description



The <code>IAMNetShowExProps</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="https://msdn.microsoft.com/e59b3086-4f62-4541-8bef-b0581f01906f">Windows Media Source</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowExProps</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMNetShowExProps</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd319723(v=VS.85).aspx">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319724(v=VS.85).aspx">get_CodecCount</a>
</td>
<td align="left" width="63%">
Retrieves the number codecs needed to play the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319725(v=VS.85).aspx">get_CreationDate</a>
</td>
<td align="left" width="63%">
Retrieves the creation date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319726(v=VS.85).aspx">get_ErrorCorrection</a>
</td>
<td align="left" width="63%">
Retrieves the error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319727(v=VS.85).aspx">get_SourceLink</a>
</td>
<td align="left" width="63%">
Retrieves the source link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319728(v=VS.85).aspx">get_SourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319720(v=VS.85).aspx">GetCodecDescription</a>
</td>
<td align="left" width="63%">
Retrieves the user-friendly description of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319721(v=VS.85).aspx">GetCodecInstalled</a>
</td>
<td align="left" width="63%">
Queries whether a specified codec is installed on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319722(v=VS.85).aspx">GetCodecURL</a>
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




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

