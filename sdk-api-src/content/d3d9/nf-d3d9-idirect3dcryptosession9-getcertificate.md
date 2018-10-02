---
UID: NF:d3d9.IDirect3DCryptoSession9.GetCertificate
title: IDirect3DCryptoSession9::GetCertificate
author: windows-sdk-content
description: Gets the driver's certificate chain.
old-location: mf\idirect3dcryptosession9_getcertificate.htm
tech.root: MedFound
ms.assetid: 802285a6-1338-4131-bb5e-9d4daad62bdc
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetCertificate method, IDirect3DCryptoSession9.GetCertificate, IDirect3DCryptoSession9::GetCertificate, d3d9/IDirect3DCryptoSession9::GetCertificate, mf.idirect3dcryptosession9_getcertificate
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
 - IDirect3DCryptoSession9.GetCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DCryptoSession9::GetCertificate


## -description


Gets the driver's certificate chain.




## -parameters




### -param CertifacteSize

The size of the <i>ppCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="https://msdn.microsoft.com/f85f3453-5bf8-412c-9ed9-e39bff496df6">IDirect3DCryptoSession9::GetCertificateSize</a>.




### -param ppCertificate

A pointer to a byte array that receives the driver's certificate chain. The caller must allocate the array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The standard key-exchange mechanism uses the driver's Output Protection Manager (OPM) certificate, which is an X.509 certificate. The type of key exchange is given in the capabilities information returned by the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a>  method. The key-exchange mechanism is specified by the <b>KeyExchangeType</b>  member of the <a href="https://msdn.microsoft.com/73ef2e12-d376-4bc2-a940-d421acfdd43e">D3DCONTENTPROTECTIONCAPS</a> structure. If the value is <b>D3DKEYEXCHANGE_RSAES_OAEP</b>, an X.509 certificate is used.

For other types of key exhange, the driver might use some other type of certificate, or might not provide a certificate.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 

