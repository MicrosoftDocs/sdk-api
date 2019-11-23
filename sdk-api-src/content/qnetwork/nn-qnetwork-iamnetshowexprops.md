---
UID: NN:qnetwork.IAMNetShowExProps
title: IAMNetShowExProps (qnetwork.h)

description: The IAMNetShowExProps interface configures the legacy Windows Media Player 6.4 source filter. The Windows Media Source filter implements this interface.
old-location: dshow\iamnetshowexprops.htm
tech.root: DirectShow
ms.assetid: e68959dc-1a79-4e2c-aeaf-3febcb9c09ce

ms.date: 12/05/2018
ms.keywords: IAMNetShowExProps, IAMNetShowExProps interface [DirectShow], IAMNetShowExProps interface [DirectShow],described, IAMNetShowExPropsInterface, dshow.iamnetshowexprops, qnetwork/IAMNetShowExProps
ms.topic: interface
f1_keywords: 
 - "qnetwork/IAMNetShowExProps"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMNetShowExProps interface


## -description



The <code>IAMNetShowExProps</code> interface configures the legacy Windows Media Player 6.4 source filter. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMNetShowExProps</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMNetShowExProps</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_bandwidth">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_codeccount">get_CodecCount</a>
</td>
<td align="left" width="63%">
Retrieves the number codecs needed to play the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_creationdate">get_CreationDate</a>
</td>
<td align="left" width="63%">
Retrieves the creation date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_errorcorrection">get_ErrorCorrection</a>
</td>
<td align="left" width="63%">
Retrieves the error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_sourcelink">get_SourceLink</a>
</td>
<td align="left" width="63%">
Retrieves the source link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_sourceprotocol">get_SourceProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the source protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-getcodecdescription">GetCodecDescription</a>
</td>
<td align="left" width="63%">
Retrieves the user-friendly description of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-getcodecinstalled">GetCodecInstalled</a>
</td>
<td align="left" width="63%">
Queries whether a specified codec is installed on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-getcodecurl">GetCodecURL</a>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

