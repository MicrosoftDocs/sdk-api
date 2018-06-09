---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetApplicationCertificate
title: IMFMediaEngineProtectedContent::SetApplicationCertificate
author: windows-sdk-content
description: Sets the application's certificate.
old-location: mf\imfmediaengineprotectedcontent_setapplicationcertificate.htm
old-project: medfound
ms.assetid: 2D1F31B1-9A4E-4B94-93FF-255B3006C904
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetApplicationCertificate method, IMFMediaEngineProtectedContent.SetApplicationCertificate, IMFMediaEngineProtectedContent::SetApplicationCertificate, SetApplicationCertificate, SetApplicationCertificate method [Media Foundation], SetApplicationCertificate method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setapplicationcertificate, mfmediaengine/IMFMediaEngineProtectedContent::SetApplicationCertificate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetApplicationCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method to access protected video content in frame-server mode.




## -see-also




<a href="https://msdn.microsoft.com/85B37711-DB46-4BC7-A051-79E9507791FA">IMFMediaEngineProtectedContent</a>
 

 

