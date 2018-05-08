---
UID: NN:wmsdkidl.IWMStreamConfig2
title: IWMStreamConfig2
author: windows-driver-content
description: The IWMStreamConfig2 interface manages the data unit extensions associated with a stream.IWMStreamConfig2 inherits from IWMStreamConfig. To obtain a pointer to IWMStreamConfig2, call the QueryInterface method of the IWMStreamConfig interface.
old-location: wmformat\iwmstreamconfig2.htm
old-project: wmformat
ms.assetid: 3ce92541-6634-4418-a7ee-f9bcaf8f42ad
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMStreamConfig2, IWMStreamConfig2 interface [windows Media Format], IWMStreamConfig2 interface [windows Media Format],described, IWMStreamConfig2Interface, wmformat.iwmstreamconfig2, wmsdkidl/IWMStreamConfig2
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
-	IWMStreamConfig2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig2 interface


## -description



The <b>IWMStreamConfig2</b> interface manages the data unit extensions associated with a stream.

<b>IWMStreamConfig2</b> inherits from <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a>. To obtain a pointer to <b>IWMStreamConfig2</b>, call the <b>QueryInterface</b> method of the <b>IWMStreamConfig</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamConfig2</b> interface inherits from <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a>. <b>IWMStreamConfig2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStreamConfig2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db84a33c-bd83-46cb-a97c-76ddeeb74927">AddDataUnitExtension</a>
</td>
<td align="left" width="63%">
Adds a data unit extension to the stream.

</td>
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
<a href="https://msdn.microsoft.com/766124f6-b376-421b-b2ee-2c280af3bd16">GetDataUnitExtension</a>
</td>
<td align="left" width="63%">
Retrieves a data unit extension from the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9a4ec84-4ea3-4e84-9def-7ca93be0f1ce">GetDataUnitExtensionCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of all the data unit extensions in the stream.

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
<a href="https://msdn.microsoft.com/dfe7b285-8d1d-4b71-a839-1c73d76e6444">GetTransportType</a>
</td>
<td align="left" width="63%">
Retrieves the type of communication protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/944c1b6c-1d1b-4a44-9b9e-d673c8d60306">RemoveAllDataUnitExtensions</a>
</td>
<td align="left" width="63%">
Removes all previously added data unit extensions.

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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89958c80-2140-49ab-b696-189e8f722e96">SetTransportType</a>
</td>
<td align="left" width="63%">
Sets the type of communication protocol.

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




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681">IWMStreamConfig3 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

