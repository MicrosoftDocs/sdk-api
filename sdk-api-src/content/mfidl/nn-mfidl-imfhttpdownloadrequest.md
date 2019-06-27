---
UID: NN:mfidl.IMFHttpDownloadRequest
title: IMFHttpDownloadRequest (mfidl.h)
author: windows-sdk-content
description: Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation.
old-location: mf\imfhttpdownloadrequest.htm
tech.root: medfound
ms.assetid: A8A37C2F-A662-4FDA-95F6-43D96A8471A8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadRequest, IMFHttpDownloadRequest interface [Media Foundation], IMFHttpDownloadRequest interface [Media Foundation],described, mf.imfhttpdownloadrequest, mfidl/IMFHttpDownloadRequest
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFHttpDownloadRequest"
req.header: mfidl.h
req.include-header: 
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFHttpDownloadRequest interface


## -description


Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadRequest</b> interface to Media Foundation through the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest">CreateRequest</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadRequest</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadRequest</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-addheader">AddHeader</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request.  Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginsendrequest">BeginSendRequest</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreadpayload">BeginReadPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to receive the message body of the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a> method. Since the size of the message body may be large, or unknown, Media Foundation may invoke this method multiple times to retrieve the message body in piecemeal fashion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreceiveresponse">BeginReceiveResponse</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endsendrequest">EndSendRequest</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginsendrequest">BeginSendRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to send a HTTP or HTTPS request

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-close">Close</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to allow <b>IMFHttpDownloadRequest</b> to free any internal resources. It will also cancel the current request if it is still in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreadpayload">EndReadPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreadpayload">BeginReadPayload</a>. When this method completes successfully, the payload data will have been written to the buffer that Media Foundation provided when invoking <b>BeginReadPayload</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreceiveresponse">BeginReceiveResponse</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endsendrequest">EndSendRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginsendrequest">BeginSendRequest</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-getatendofpayload">GetAtEndOfPayload</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to check if it should invoke <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreadpayload">BeginReadPayload</a> to read data from the message body of the response. During the processing of a typical HTTP response, Media Foundation will invoke <b>BeginReadPayload</b> multiple times, but once <b>GetAtEndOfPayload</b> sets its output parameter to TRUE, Media Foundation will not invoke <b>BeginReadPayload</b> again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-gethttpstatus">GetHttpStatus</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-getrangeendoffset">GetRangeEndOffset</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the offset of the last byte in the current response, counted from the start of the resource. This is useful when a request uses the HTTP “Range” header to download only a portion of a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-gettimeseekresult">GetTimeSeekResult</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the values of the TimeSeekRange.DLNA.ORG HTTP header, if any, that the server specified in its response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-gettotallength">GetTotalLength</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the total length of the resource that is being downloaded, if known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-geturl">GetURL</a>
</td>
<td align="left" width="63%">
Returns the URL that is used for sending the request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-hasnullsourceorigin">HasNullSourceOrigin</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to detect the case when a HTTP or HTTPS request has been redirected to a different server of different "origin". 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-queryheader">QueryHeader</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a> method.

</td>
</tr>
</table> 

