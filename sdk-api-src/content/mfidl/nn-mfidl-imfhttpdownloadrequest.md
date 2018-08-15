---
UID: NN:mfidl.IMFHttpDownloadRequest
title: IMFHttpDownloadRequest
author: windows-sdk-content
description: Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation.
old-location: mf\imfhttpdownloadrequest.htm
old-project: medfound
ms.assetid: A8A37C2F-A662-4FDA-95F6-43D96A8471A8
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFHttpDownloadRequest, IMFHttpDownloadRequest interface [Media Foundation], IMFHttpDownloadRequest interface [Media Foundation],described, mf.imfhttpdownloadrequest, mfidl/IMFHttpDownloadRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFHttpDownloadRequest
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadRequest interface


## -description


Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadRequest</b> interface to Media Foundation through the <a href="https://msdn.microsoft.com/111A075A-82A7-4607-9359-37B2DA97AFC5">CreateRequest</a> method on the <a href="https://msdn.microsoft.com/048B2922-3B77-4F2D-9437-0FA54F94C67E">IMFHttpDownloadSession</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadRequest</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFHttpDownloadRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFHttpDownloadRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37A2C9D8-EFF6-49D5-B495-EDBEEABD59CE">AddHeader</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request.  Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the <a href="https://msdn.microsoft.com/38025B19-146A-4050-9BD2-2CF974729FE3">BeginSendRequest</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to receive the message body of the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a> method. Since the size of the message body may be large, or unknown, Media Foundation may invoke this method multiple times to retrieve the message body in piecemeal fashion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6D5DB091-426B-4E89-8657-0BDC6427B23A">BeginReceiveResponse</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://msdn.microsoft.com/2B1554C7-2814-4A9E-BBAC-B25C78775420">EndSendRequest</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38025B19-146A-4050-9BD2-2CF974729FE3">BeginSendRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to send a HTTP or HTTPS request

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BA560323-EE64-4423-B63A-F2B6FDE608DC">Close</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to allow <b>IMFHttpDownloadRequest</b> to free any internal resources. It will also cancel the current request if it is still in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/491437FE-1401-4841-AE0E-428F28E34D4D">EndReadPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a>. When this method completes successfully, the payload data will have been written to the buffer that Media Foundation provided when invoking <b>BeginReadPayload</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://msdn.microsoft.com/6D5DB091-426B-4E89-8657-0BDC6427B23A">BeginReceiveResponse</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B1554C7-2814-4A9E-BBAC-B25C78775420">EndSendRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://msdn.microsoft.com/38025B19-146A-4050-9BD2-2CF974729FE3">BeginSendRequest</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F2D65BA-4719-4633-9B2D-2CAF88F4E3DD">GetAtEndOfPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to check if it should invoke <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a> to read data from the message body of the response. During the processing of a typical HTTP response, Media Foundation will invoke <b>BeginReadPayload</b> multiple times, but once <b>GetAtEndOfPayload</b> sets its output parameter to TRUE, Media Foundation will not invoke <b>BeginReadPayload</b> again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E084CF25-BEFA-4061-AA77-2CFC57CF6DCE">GetHttpStatus</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/015CBC40-BE9E-4C9F-AC1B-30FFDD2B11CC">GetRangeEndOffset</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the offset of the last byte in the current response, counted from the start of the resource. This is useful when a request uses the HTTP “Range” header to download only a portion of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7647460-8BAA-4480-A296-D83DFFBC5800">GetTimeSeekResult</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the values of the TimeSeekRange.DLNA.ORG HTTP header, if any, that the server specified in its response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E52D44B5-F24F-4234-A67D-0F764A3864DB">GetTotalLength</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the total length of the resource that is being downloaded, if known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38FAD6B8-8C50-492C-BC53-6F301D49083F">GetURL</a>
</td>
<td align="left" width="63%">
Returns the URL that is used for sending the request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D83F079F-605A-4F62-B037-3C5D0487D778">HasNullSourceOrigin</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to detect the case when a HTTP or HTTPS request has been redirected to a different server of different "origin". 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BFAE5257-0BE8-47F3-B3CD-490885E60065">QueryHeader</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a> method.

</td>
</tr>
</table> 

