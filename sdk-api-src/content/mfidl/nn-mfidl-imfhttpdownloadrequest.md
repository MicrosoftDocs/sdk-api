---
UID: NN:mfidl.IMFHttpDownloadRequest
title: IMFHttpDownloadRequest (mfidl.h)
description: Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. (IMFHttpDownloadRequest)
helpviewer_keywords: ["IMFHttpDownloadRequest","IMFHttpDownloadRequest interface [Media Foundation]","IMFHttpDownloadRequest interface [Media Foundation]","described","mf.imfhttpdownloadrequest","mfidl/IMFHttpDownloadRequest"]
old-location: mf\imfhttpdownloadrequest.htm
tech.root: mf
ms.assetid: A8A37C2F-A662-4FDA-95F6-43D96A8471A8
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadRequest, IMFHttpDownloadRequest interface [Media Foundation], IMFHttpDownloadRequest interface [Media Foundation],described, mf.imfhttpdownloadrequest, mfidl/IMFHttpDownloadRequest
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
 - IMFHttpDownloadRequest
 - mfidl/IMFHttpDownloadRequest
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
 - IMFHttpDownloadRequest
---

# IMFHttpDownloadRequest interface


## -description

Applications implement this interface to override the default implementation of the HTTP and HTTPS protocols used by Microsoft Media Foundation. Applications provide the <b>IMFHttpDownloadRequest</b> interface to Media Foundation through the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest">CreateRequest</a> method on the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> interface.

## -inheritance

The <b>IMFHttpDownloadRequest</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadRequest</b> also has these types of members:

