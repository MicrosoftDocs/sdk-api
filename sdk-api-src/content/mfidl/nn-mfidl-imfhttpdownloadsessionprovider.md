---
UID: NN:mfidl.IMFHttpDownloadSessionProvider
title: IMFHttpDownloadSessionProvider (mfidl.h)
description: Applications implement this interface in order to provide custom a custom HTTP or HTTPS download implementation.
old-location: mf\imfhttpdownloadsessionprovider.htm
tech.root: medfound
ms.assetid: 4A3A96FB-A7C5-40BB-AB8F-12A7F00FDCD1
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadSessionProvider, IMFHttpDownloadSessionProvider interface [Media Foundation], IMFHttpDownloadSessionProvider interface [Media Foundation],described, mf.imfhttpdownloadsessionprovider, mfidl/IMFHttpDownloadSessionProvider
ms.topic: interface
f1_keywords:
- mfidl/IMFHttpDownloadSessionProvider
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
- IMFHttpDownloadSessionProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFHttpDownloadSessionProvider interface


## -description


Applications implement this interface in order to provide custom a custom HTTP or HTTPS download implementation. Use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a> interface to register the provider. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-source-resolver">Using the Source Resolver</a>. Once registered, the Microsoft Media Foundation will invoke the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession">CreateHttpDownloadSession</a> method of the provider  implementation to open HTTP or HTTPS URLs instead of using the default implementation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFHttpDownloadSessionProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadSessionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFHttpDownloadSessionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession">CreateHttpDownloadSession</a>
</td>
<td align="left" width="63%">
Called by the Microsoft Media Foundation to open HTTP or HTTPS URLs instead of using the default implementation.

</td>
</tr>
</table> 

