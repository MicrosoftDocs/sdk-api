---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetApplicationCertificate
title: IMFMediaEngineProtectedContent::SetApplicationCertificate (mfmediaengine.h)
description: Sets the application's certificate.
helpviewer_keywords: ["IMFMediaEngineProtectedContent interface [Media Foundation]","SetApplicationCertificate method","IMFMediaEngineProtectedContent.SetApplicationCertificate","IMFMediaEngineProtectedContent::SetApplicationCertificate","SetApplicationCertificate","SetApplicationCertificate method [Media Foundation]","SetApplicationCertificate method [Media Foundation]","IMFMediaEngineProtectedContent interface","mf.imfmediaengineprotectedcontent_setapplicationcertificate","mfmediaengine/IMFMediaEngineProtectedContent::SetApplicationCertificate"]
old-location: mf\imfmediaengineprotectedcontent_setapplicationcertificate.htm
tech.root: mf
ms.assetid: 2D1F31B1-9A4E-4B94-93FF-255B3006C904
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetApplicationCertificate method, IMFMediaEngineProtectedContent.SetApplicationCertificate, IMFMediaEngineProtectedContent::SetApplicationCertificate, SetApplicationCertificate, SetApplicationCertificate method [Media Foundation], SetApplicationCertificate method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setapplicationcertificate, mfmediaengine/IMFMediaEngineProtectedContent::SetApplicationCertificate
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineProtectedContent::SetApplicationCertificate
 - mfmediaengine/IMFMediaEngineProtectedContent::SetApplicationCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetApplicationCertificate
---

# IMFMediaEngineProtectedContent::SetApplicationCertificate


## -description

Sets the application's certificate.

## -parameters

### -param pbBlob [in]

A pointer to a buffer that contains the certificate in X.509 format, followed by the application identifier signed with a SHA-256 signature using the private key from the certificate.

### -param cbBlob [in]

The size of the <i>pbBlob</i> buffer, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method to access protected video content in frame-server mode.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>