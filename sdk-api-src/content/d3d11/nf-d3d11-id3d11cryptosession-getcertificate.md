---
UID: NF:d3d11.ID3D11CryptoSession.GetCertificate
title: ID3D11CryptoSession::GetCertificate
author: windows-driver-content
description: Gets the driver's certificate chain.
old-location: mf\id3d11cryptosession_getcertificate.htm
old-project: medfound
ms.assetid: D6407570-62C0-45D0-9BCB-41EA007D86A6
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCertificate method, ID3D11CryptoSession.GetCertificate, ID3D11CryptoSession::GetCertificate, d3d11/ID3D11CryptoSession::GetCertificate, mf.id3d11cryptosession_getcertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11CryptoSession.GetCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11CryptoSession::GetCertificate


## -description


Gets the driver's certificate chain.


## -parameters




### -param CertificateSize [in]

The size of the <i>pCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="https://msdn.microsoft.com/C5FE51B8-A681-4B8C-BFC0-9D0B625292F1">ID3D11CryptoSession::GetCertificateSize</a>.


### -param pCertificate [out]

A pointer to a byte array that receives the driver's certificate chain. The caller must allocate the array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a>
 

 

