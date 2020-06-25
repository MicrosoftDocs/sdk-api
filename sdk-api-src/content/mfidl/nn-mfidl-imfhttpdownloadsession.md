---
UID: NN:mfidl.IMFHttpDownloadSession
title: IMFHttpDownloadSession (mfidl.h)
description: Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation.
helpviewer_keywords: ["IMFHttpDownloadSession","IMFHttpDownloadSession interface [Media Foundation]","IMFHttpDownloadSession interface [Media Foundation]","described","mf.imfhttpdownloadsession","mfidl/IMFHttpDownloadSession"]
old-location: mf\imfhttpdownloadsession.htm
tech.root: medfound
ms.assetid: 048B2922-3B77-4F2D-9437-0FA54F94C67E
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadSession, IMFHttpDownloadSession interface [Media Foundation], IMFHttpDownloadSession interface [Media Foundation],described, mf.imfhttpdownloadsession, mfidl/IMFHttpDownloadSession
f1_keywords:
- mfidl/IMFHttpDownloadSession
dev_langs:
- c++
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
- IMFHttpDownloadSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFHttpDownloadSession interface


## -description


Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadSession</b> interface to Media Foundation through the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession">CreateHttpDownloadSession</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider">IMFHttpDownloadSessionProvider</a> interface. Microsoft Media Foundation uses this interface to perform a “streaming”, or “progressive”, download of a resource identified by a HTTP or HTTPS URL. Multiple HTTP requests may be sent to download the resource. The <b>IMFHttpDownloadSession</b> interface is used to create these individual HTTP requests.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadSession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFHttpDownloadSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-close">Close</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to specify that no more HTTP requests will be created, and allows <b>IMFHttpDownloadSession</b> to free any internal resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest">CreateRequest</a>
</td>
<td align="left" width="63%">
Invoked by Microsoft Media Foundation to create an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a> interface, which is used to send a single HTTP, or HTTPS request. Since multiple requests may be needed to fully download a resource, Media Foundation may invoke <b>CreateRequest</b> multiple times on the same <b>IMFHttpDownloadSession</b> instance. Media Foundation will use each <b>IMFHttpDownloadRequest</b> instance for only a single request. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-setserver">SetServer</a>
</td>
<td align="left" width="63%">
Called  by Microsoft Media Foundation to specify parameters common to all requests created by this instance of <b>IMFHttpDownloadSession</b>.

</td>
</tr>
</table> 

