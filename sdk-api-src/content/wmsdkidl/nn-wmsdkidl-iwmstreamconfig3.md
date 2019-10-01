---
UID: NN:wmsdkidl.IWMStreamConfig3
title: IWMStreamConfig3 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMStreamConfig3 interface controls language settings for a stream.An IWMStreamConfig3 interface exists for every stream configuration object.
old-location: wmformat\iwmstreamconfig3.htm
tech.root: wmformat
ms.assetid: c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig3, IWMStreamConfig3 interface [windows Media Format], IWMStreamConfig3 interface [windows Media Format],described, IWMStreamConfig3Interface, wmformat.iwmstreamconfig3, wmsdkidl/IWMStreamConfig3
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMStreamConfig3"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig3 interface


## -description



The <b>IWMStreamConfig3</b> interface controls language settings for a stream.

An <b>IWMStreamConfig3</b> interface exists for every stream configuration object. You can obtain a pointer to an <b>IWMStreamConfig3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the stream configuration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStreamConfig3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2</a>. <b>IWMStreamConfig3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension">AddDataUnitExtension</a>
</td>
<td align="left" width="63%">
Adds a data unit extension to the stream.

</td>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension">GetDataUnitExtension</a>
</td>
<td align="left" width="63%">
Retrieves a data unit extension from the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount">GetDataUnitExtensionCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of all the data unit extensions in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-getlanguage">GetLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the language setting for the stream.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-gettransporttype">GetTransportType</a>
</td>
<td align="left" width="63%">
Retrieves the type of communication protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-removealldataunitextensions">RemoveAllDataUnitExtensions</a>
</td>
<td align="left" width="63%">
Removes all previously added data unit extensions.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage">SetLanguage</a>
</td>
<td align="left" width="63%">
Configures the language setting for the stream.

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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-settransporttype">SetTransportType</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a>
</td>
<td>IID_IWMStreamConfig</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

