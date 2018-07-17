---
UID: NN:wmsdkidl.IWMStreamConfig
title: IWMStreamConfig
author: windows-sdk-content
description: The IWMStreamConfig interface is the primary interface of a stream configuration object.
old-location: wmformat\iwmstreamconfig.htm
old-project: wmformat
ms.assetid: e013996a-95b6-4cd3-9fb5-75dbce821eef
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMStreamConfig, IWMStreamConfig interface [windows Media Format], IWMStreamConfig interface [windows Media Format],described, IWMStreamConfigInterface, wmformat.iwmstreamconfig, wmsdkidl/IWMStreamConfig
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMStreamConfig
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig interface


## -description



The <b>IWMStreamConfig</b> interface is the primary interface of a stream configuration object. It provides methods to configure basic properties for streams to be used in a profile.

Every profile contains one or more stream configuration objects. You can get the <b>IWMStreamConfig</b> interface of a stream configuration object by calling the <a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">IWMProfile::GetStream</a> method or the <a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">IWMProfile::GetStreamByNumber</a> method. The difference between these two methods is that <b>GetStream</b> retrieves the stream using an index ranging from zero to one less than the total stream count, and <b>GetStreamByNumber</b> retrieves the stream using the assigned stream number. You can also retrieve a stream configuration object using the <a href="https://msdn.microsoft.com/4a1478ff-00fb-46e2-97a3-e00e9c1b819a">IWMProfile::CreateNewStream</a> method. All of the methods that create stream configuration objects set a pointer to this interface.

<div class="alert"><b>Important</b>  After calling one or more of the <b>IWMStreamConfig::Set...</b> methods, you must call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a> for all the changes to take effect in the profile.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMStreamConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStreamConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d34bea45-758e-4c4a-928f-229ce6b4241c">GetBitrate</a>
</td>
<td align="left" width="63%">
Retrieves the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a78cd61-e7ae-42e2-9d64-f3344fefc59d">GetBufferWindow</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04d50606-c355-45d4-9cc1-a8ef37113bf7">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the connection name given to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86c65cfe-d482-461b-a187-ce1ce9a30609">GetStreamName</a>
</td>
<td align="left" width="63%">
Retrieves the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2996c897-eb38-4432-8bf7-549023ab00f5">GetStreamNumber</a>
</td>
<td align="left" width="63%">
Retrieves the stream number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8dc8c37-da52-4d0f-b143-aaa45e6f77b8">GetStreamType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the stream (audio, video, or script).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/202be688-e739-4e80-9574-f85b2eb168fc">SetBitrate</a>
</td>
<td align="left" width="63%">
Specifies the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae14f3df-222a-494c-a171-02aed04490d1">SetBufferWindow</a>
</td>
<td align="left" width="63%">
Specifies the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd67e0b5-3bfa-46c1-996d-6b026c1144cb">SetConnectionName</a>
</td>
<td align="left" width="63%">
Specifies the connection name given to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90ab1591-eee7-4504-8d7f-475d90fa3b40">SetStreamName</a>
</td>
<td align="left" width="63%">
Specifies the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aea8b219-5b47-4176-ad96-d52646d96578">SetStreamNumber</a>
</td>
<td align="left" width="63%">
Specifies the stream number.

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
<tr>
<td>
<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681">IWMStreamConfig3 Interface</a>



<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

