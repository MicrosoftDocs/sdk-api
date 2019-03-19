---
UID: NN:wmsdkidl.IWMStreamConfig
title: IWMStreamConfig (wmsdkidl.h)
author: windows-sdk-content
description: The IWMStreamConfig interface is the primary interface of a stream configuration object.
old-location: wmformat\iwmstreamconfig.htm
tech.root: wmformat
ms.assetid: e013996a-95b6-4cd3-9fb5-75dbce821eef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMStreamConfig, IWMStreamConfig interface [windows Media Format], IWMStreamConfig interface [windows Media Format],described, IWMStreamConfigInterface, wmformat.iwmstreamconfig, wmsdkidl/IWMStreamConfig
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
 - IWMStreamConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamConfig interface


## -description



The <b>IWMStreamConfig</b> interface is the primary interface of a stream configuration object. It provides methods to configure basic properties for streams to be used in a profile.

Every profile contains one or more stream configuration objects. You can get the <b>IWMStreamConfig</b> interface of a stream configuration object by calling the <a href="https://msdn.microsoft.com/en-us/library/Dd757406(v=VS.85).aspx">IWMProfile::GetStream</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Dd757407(v=VS.85).aspx">IWMProfile::GetStreamByNumber</a> method. The difference between these two methods is that <b>GetStream</b> retrieves the stream using an index ranging from zero to one less than the total stream count, and <b>GetStreamByNumber</b> retrieves the stream using the assigned stream number. You can also retrieve a stream configuration object using the <a href="https://msdn.microsoft.com/en-us/library/Dd757401(v=VS.85).aspx">IWMProfile::CreateNewStream</a> method. All of the methods that create stream configuration objects set a pointer to this interface.

<div class="alert"><b>Important</b>  After calling one or more of the <b>IWMStreamConfig::Set...</b> methods, you must call <a href="https://msdn.microsoft.com/en-us/library/Dd757410(v=VS.85).aspx">IWMProfile::ReconfigStream</a> for all the changes to take effect in the profile.</div>
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
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798711(v=VS.85).aspx">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757209(v=VS.85).aspx">IWMInputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757252(v=VS.85).aspx">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798547(v=VS.85).aspx">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798554(v=VS.85).aspx">IWMStreamConfig3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798711(v=VS.85).aspx">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

