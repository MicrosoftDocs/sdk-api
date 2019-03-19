---
UID: NF:d3d11.ID3D11CryptoSession.GetCertificateSize
title: ID3D11CryptoSession::GetCertificateSize (d3d11.h)
author: windows-sdk-content
description: Gets the size of the driver's certificate chain.
old-location: mf\id3d11cryptosession_getcertificatesize.htm
tech.root: medfound
ms.assetid: C5FE51B8-A681-4B8C-BFC0-9D0B625292F1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCertificateSize method, ID3D11CryptoSession.GetCertificateSize, ID3D11CryptoSession::GetCertificateSize, d3d11/ID3D11CryptoSession::GetCertificateSize, mf.id3d11cryptosession_getcertificatesize
ms.topic: method
req.header: d3d11.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11CryptoSession.GetCertificateSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11CryptoSession::GetCertificateSize


## -description


Gets the size of the driver's certificate chain.


## -parameters




### -param pCertificateSize [out]

Receives the size of the certificate chain, in bytes.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the certificate, call <a href="https://msdn.microsoft.com/D6407570-62C0-45D0-9BCB-41EA007D86A6">ID3D11CryptoSession::GetCertificate</a>.




## -see-also




<a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a>
 

 

