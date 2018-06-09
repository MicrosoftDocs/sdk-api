---
UID: NN:wmcontainer.IMFASFStreamSelector
title: IMFASFStreamSelector
author: windows-sdk-content
description: Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header.
old-location: mf\imfasfstreamselector.htm
old-project: medfound
ms.assetid: d2e1fc15-2e12-4698-a4b1-ca8046d228de
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFASFStreamSelector, IMFASFStreamSelector interface [Media Foundation], IMFASFStreamSelector interface [Media Foundation],described, d2e1fc15-2e12-4698-a4b1-ca8046d228de, mf.imfasfstreamselector, wmcontainer/IMFASFStreamSelector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamSelector
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamSelector interface


## -description


Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header. The ASF stream selector object exposes this interface. To create the ASF stream selector, call <a href="https://msdn.microsoft.com/71b1af5b-f127-463f-9720-72e789bb2cd1">MFCreateASFStreamSelector</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFStreamSelector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFStreamSelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFStreamSelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2debbce-f6ee-45d7-bf05-2b07aa7719c7">BitrateToStepNumber</a>
</td>
<td align="left" width="63%">
Retrieves the index of a bandwidth step that is appropriate for a specified bit rate. This method is used for multiple bit rate (MBR) content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c">GetBandwidthStep</a>
</td>
<td align="left" width="63%">
Retrieves the stream numbers that apply to a bandwidth step. This method is used for MBR content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b7105c1-7395-462f-ad52-daf621258714">GetBandwidthStepCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of bandwidth steps that exist for the content. This method is used for MBR content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09f00f52-f897-46f0-afb9-ae59913e04a1">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of outputs for the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7ff421b-3ef3-406a-ae05-8d8bf9f4357f">GetOutputFromStream</a>
</td>
<td align="left" width="63%">
Retrieves the output number associated with a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d134f4a9-9bca-454f-8dc1-2e152684a4bf">GetOutputMutex</a>
</td>
<td align="left" width="63%">
Retrieves a mutual exclusion object for an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6e98595-3307-47f5-806d-796350c78cec">GetOutputMutexCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of mutual exclusion objects associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64413669-bcb9-47fa-9362-b3f6831e55fb">GetOutputOverride</a>
</td>
<td align="left" width="63%">
Retrieves the manual output override selection that is set for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/928e958b-55dc-4939-8ac3-282389f0077a">GetOutputStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a999e7a-1b2e-4206-874a-ed93b868150b">GetOutputStreamNumbers</a>
</td>
<td align="left" width="63%">
Retrieves the stream numbers for all of the streams that are associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1e80c32-bfd4-4404-9ccc-05b5077b83a6">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams that are in the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eebaf4a4-fcd5-4438-82ec-e9da2de6b0fd">SetOutputMutexSelection</a>
</td>
<td align="left" width="63%">
Selects a mutual exclusion record to use for a mutual exclusion object associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8affecd-107f-4701-88df-200db06ad49e">SetOutputOverride</a>
</td>
<td align="left" width="63%">
Sets the selection status of an output, overriding other selection criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2a0f318-0de2-49e0-b8f2-847ab1371752">SetStreamSelectorFlags</a>
</td>
<td align="left" width="63%">
Sets options for the stream selector.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

