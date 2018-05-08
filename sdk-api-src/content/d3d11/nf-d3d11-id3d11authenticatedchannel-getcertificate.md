---
UID: NF:d3d11.ID3D11AuthenticatedChannel.GetCertificate
title: ID3D11AuthenticatedChannel::GetCertificate
author: windows-driver-content
description: Gets the driver's certificate chain.
old-location: mf\id3d11authenticatedchannel_getcertificate.htm
old-project: medfound
ms.assetid: D7FC07CA-B045-4C44-B3FD-B902C5437E47
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],ID3D11AuthenticatedChannel interface, ID3D11AuthenticatedChannel interface [Media Foundation],GetCertificate method, ID3D11AuthenticatedChannel.GetCertificate, ID3D11AuthenticatedChannel::GetCertificate, d3d11/ID3D11AuthenticatedChannel::GetCertificate, mf.id3d11authenticatedchannel_getcertificate
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
-	ID3D11AuthenticatedChannel.GetCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11AuthenticatedChannel::GetCertificate


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




<a href="https://msdn.microsoft.com/library/windows/hardware/hh451654">GetCertificateSize</a>



<a href="https://msdn.microsoft.com/B2DE8E06-1571-4D50-9296-8EB4BB74D6BA">ID3D11AuthenticatedChannel</a>
 

 

