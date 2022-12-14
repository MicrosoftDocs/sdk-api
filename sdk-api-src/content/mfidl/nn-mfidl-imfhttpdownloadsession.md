---
UID: NN:mfidl.IMFHttpDownloadSession
title: IMFHttpDownloadSession (mfidl.h)
description: Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. (IMFHttpDownloadSession)
helpviewer_keywords: ["IMFHttpDownloadSession","IMFHttpDownloadSession interface [Media Foundation]","IMFHttpDownloadSession interface [Media Foundation]","described","mf.imfhttpdownloadsession","mfidl/IMFHttpDownloadSession"]
old-location: mf\imfhttpdownloadsession.htm
tech.root: mf
ms.assetid: 048B2922-3B77-4F2D-9437-0FA54F94C67E
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadSession, IMFHttpDownloadSession interface [Media Foundation], IMFHttpDownloadSession interface [Media Foundation],described, mf.imfhttpdownloadsession, mfidl/IMFHttpDownloadSession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFHttpDownloadSession
 - mfidl/IMFHttpDownloadSession
dev_langs:
 - c++
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
---

# IMFHttpDownloadSession interface


## -description

Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadSession</b> interface to Media Foundation through the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession">CreateHttpDownloadSession</a> method on the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider">IMFHttpDownloadSessionProvider</a> interface. Microsoft Media Foundation uses this interface to perform a “streaming”, or “progressive”, download of a resource identified by a HTTP or HTTPS URL. Multiple HTTP requests may be sent to download the resource. The <b>IMFHttpDownloadSession</b> interface is used to create these individual HTTP requests.

## -inheritance

The <b>IMFHttpDownloadSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadSession</b> also has these types of members:

