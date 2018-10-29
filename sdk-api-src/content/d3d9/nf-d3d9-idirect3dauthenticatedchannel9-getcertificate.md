---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.GetCertificate
title: IDirect3DAuthenticatedChannel9::GetCertificate
author: windows-sdk-content
description: Gets the driver's certificate chain.
old-location: mf\idirect3dauthenticatedchannel9_getcertificate.htm
tech.root: medfound
ms.assetid: 0663d3a0-256b-4c96-aca7-06c4d1853554
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],GetCertificate method, IDirect3DAuthenticatedChannel9.GetCertificate, IDirect3DAuthenticatedChannel9::GetCertificate, d3d9/IDirect3DAuthenticatedChannel9::GetCertificate, mf.idirect3dauthenticatedchannel9_getcertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - d3d9.h
api_name:
 - IDirect3DAuthenticatedChannel9.GetCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DAuthenticatedChannel9::GetCertificate


## -description


Gets the driver's certificate chain.


## -parameters




### -param CertifacteSize

The size of the <i>ppCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="https://msdn.microsoft.com/a320a7be-6a0f-4de1-afc2-11eb2d7c24d6">IDirect3DAuthenticatedChannel9::GetCertificateSize</a>.


### -param ppCertificate

A pointer to a byte array that receives the driver's X.509 certificate chain. The caller must allocate the array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the certificate chain to verify that the driver's certificate was signed by Microsoft and has not been revoked. The driver's certificate also contains the driver's public key. Use the public key to establish a session key, by calling the <a href="https://msdn.microsoft.com/35605d35-76c9-43d7-a022-6db6af179c41">IDirect3DAuthenticatedChannel9::NegotiateKeyExchange</a> method.

This method fails if the channel type is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, because the Direct3D 9 channel does not support authentication.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
 

 

