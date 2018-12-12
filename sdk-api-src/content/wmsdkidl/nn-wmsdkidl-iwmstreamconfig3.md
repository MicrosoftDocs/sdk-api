---
UID: NN:wmsdkidl.IWMStreamConfig3
title: IWMStreamConfig3
author: windows-sdk-content
description: The IWMStreamConfig3 interface controls language settings for a stream.An IWMStreamConfig3 interface exists for every stream configuration object.
old-location: wmformat\iwmstreamconfig3.htm
tech.root: wmformat
ms.assetid: c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMStreamConfig3, IWMStreamConfig3 interface [windows Media Format], IWMStreamConfig3 interface [windows Media Format],described, IWMStreamConfig3Interface, wmformat.iwmstreamconfig3, wmsdkidl/IWMStreamConfig3
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
 - IWMStreamConfig3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamConfig3 interface


## -description



The <b>IWMStreamConfig3</b> interface controls language settings for a stream.

An <b>IWMStreamConfig3</b> interface exists for every stream configuration object. You can obtain a pointer to an <b>IWMStreamConfig3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the stream configuration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamConfig3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd798547(v=VS.85).aspx">IWMStreamConfig2</a>. <b>IWMStreamConfig3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStreamConfig3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798548(v=VS.85).aspx">AddDataUnitExtension</a>
</td>
<td align="left" width="63%">
Adds a data unit extension to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798558(v=VS.85).aspx">GetBitrate</a>
</td>
<td align="left" width="63%">
Retrieves the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798559(v=VS.85).aspx">GetBufferWindow</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798560(v=VS.85).aspx">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the connection name given to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798549(v=VS.85).aspx">GetDataUnitExtension</a>
</td>
<td align="left" width="63%">
Retrieves a data unit extension from the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798550(v=VS.85).aspx">GetDataUnitExtensionCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of all the data unit extensions in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798556(v=VS.85).aspx">GetLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language setting for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798561(v=VS.85).aspx">GetStreamName</a>
</td>
<td align="left" width="63%">
Retrieves the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798562(v=VS.85).aspx">GetStreamNumber</a>
</td>
<td align="left" width="63%">
Retrieves the stream number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798563(v=VS.85).aspx">GetStreamType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the stream (audio, video, or script).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798551(v=VS.85).aspx">GetTransportType</a>
</td>
<td align="left" width="63%">
Retrieves the type of communication protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798552(v=VS.85).aspx">RemoveAllDataUnitExtensions</a>
</td>
<td align="left" width="63%">
Removes all previously added data unit extensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798564(v=VS.85).aspx">SetBitrate</a>
</td>
<td align="left" width="63%">
Specifies the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798565(v=VS.85).aspx">SetBufferWindow</a>
</td>
<td align="left" width="63%">
Specifies the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798566(v=VS.85).aspx">SetConnectionName</a>
</td>
<td align="left" width="63%">
Specifies the connection name given to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798557(v=VS.85).aspx">SetLanguage</a>
</td>
<td align="left" width="63%">
Configures the language setting for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798567(v=VS.85).aspx">SetStreamName</a>
</td>
<td align="left" width="63%">
Specifies the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798568(v=VS.85).aspx">SetStreamNumber</a>
</td>
<td align="left" width="63%">
Specifies the stream number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd798553(v=VS.85).aspx">SetTransportType</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798711(v=VS.85).aspx">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798547(v=VS.85).aspx">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

