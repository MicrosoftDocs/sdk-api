---
UID: NN:wmsdkidl.IWMStreamConfig
title: IWMStreamConfig (wmsdkidl.h)
author: windows-sdk-content
description: The IWMStreamConfig interface is the primary interface of a stream configuration object.
old-location: wmformat\iwmstreamconfig.htm
tech.root: wmformat
ms.assetid: e013996a-95b6-4cd3-9fb5-75dbce821eef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig, IWMStreamConfig interface [windows Media Format], IWMStreamConfig interface [windows Media Format],described, IWMStreamConfigInterface, wmformat.iwmstreamconfig, wmsdkidl/IWMStreamConfig
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMStreamConfig"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig interface


## -description



The <b>IWMStreamConfig</b> interface is the primary interface of a stream configuration object. It provides methods to configure basic properties for streams to be used in a profile.

Every profile contains one or more stream configuration objects. You can get the <b>IWMStreamConfig</b> interface of a stream configuration object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">IWMProfile::GetStream</a> method or the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">IWMProfile::GetStreamByNumber</a> method. The difference between these two methods is that <b>GetStream</b> retrieves the stream using an index ranging from zero to one less than the total stream count, and <b>GetStreamByNumber</b> retrieves the stream using the assigned stream number. You can also retrieve a stream configuration object using the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">IWMProfile::CreateNewStream</a> method. All of the methods that create stream configuration objects set a pointer to this interface.

<div class="alert"><b>Important</b>  After calling one or more of the <b>IWMStreamConfig::Set...</b> methods, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a> for all the changes to take effect in the profile.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getbitrate">GetBitrate</a>
</td>
<td align="left" width="63%">
Retrieves the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getbufferwindow">GetBufferWindow</a>
</td>
<td align="left" width="63%">
Retrieves the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the connection name given to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamname">GetStreamName</a>
</td>
<td align="left" width="63%">
Retrieves the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamnumber">GetStreamNumber</a>
</td>
<td align="left" width="63%">
Retrieves the stream number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamtype">GetStreamType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the stream (audio, video, or script).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate">SetBitrate</a>
</td>
<td align="left" width="63%">
Specifies the bit rate for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow">SetBufferWindow</a>
</td>
<td align="left" width="63%">
Specifies the maximum latency between when a stream is received and when it begins to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname">SetConnectionName</a>
</td>
<td align="left" width="63%">
Specifies the connection name given to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname">SetStreamName</a>
</td>
<td align="left" width="63%">
Specifies the stream name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber">SetStreamNumber</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>
</td>
<td>IID_IWMMediaProps</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault">IWMPropertyVault</a>
</td>
<td>IID_IWMPropertyVault</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3</a>
</td>
<td>IID_IWMStreamConfig3</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
 

 

