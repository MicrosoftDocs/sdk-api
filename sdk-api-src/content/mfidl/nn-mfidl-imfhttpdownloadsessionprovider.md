---
UID: NN:mfidl.IMFHttpDownloadSessionProvider
title: IMFHttpDownloadSessionProvider (mfidl.h)
description: Applications implement this interface in order to provide custom a custom HTTP or HTTPS download implementation.
helpviewer_keywords: ["IMFHttpDownloadSessionProvider","IMFHttpDownloadSessionProvider interface [Media Foundation]","IMFHttpDownloadSessionProvider interface [Media Foundation]","described","mf.imfhttpdownloadsessionprovider","mfidl/IMFHttpDownloadSessionProvider"]
old-location: mf\imfhttpdownloadsessionprovider.htm
tech.root: mf
ms.assetid: 4A3A96FB-A7C5-40BB-AB8F-12A7F00FDCD1
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadSessionProvider, IMFHttpDownloadSessionProvider interface [Media Foundation], IMFHttpDownloadSessionProvider interface [Media Foundation],described, mf.imfhttpdownloadsessionprovider, mfidl/IMFHttpDownloadSessionProvider
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
 - IMFHttpDownloadSessionProvider
 - mfidl/IMFHttpDownloadSessionProvider
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
 - IMFHttpDownloadSessionProvider
---

# IMFHttpDownloadSessionProvider interface


## -description

Applications implement this interface in order to provide custom a custom HTTP or HTTPS download implementation. Use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a> interface to register the provider. For more information, see <a href="/windows/desktop/medfound/using-the-source-resolver">Using the Source Resolver</a>. Once registered, the Microsoft Media Foundation will invoke the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession">CreateHttpDownloadSession</a> method of the provider  implementation to open HTTP or HTTPS URLs instead of using the default implementation.

## -inheritance

The <b>IMFHttpDownloadSessionProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFHttpDownloadSessionProvider</b> also has these types of members:

