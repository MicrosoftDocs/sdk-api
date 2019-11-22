---
UID: NF:d3d9.IDirect3DCryptoSession9.GetCertificateSize
title: IDirect3DCryptoSession9::GetCertificateSize (d3d9.h)

description: Gets the size of the driver's certificate chain.
old-location: mf\idirect3dcryptosession9_getcertificatesize.htm
tech.root: medfound
ms.assetid: f85f3453-5bf8-412c-9ed9-e39bff496df6

ms.date: 12/05/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetCertificateSize method, IDirect3DCryptoSession9.GetCertificateSize, IDirect3DCryptoSession9::GetCertificateSize, d3d9/IDirect3DCryptoSession9::GetCertificateSize, mf.idirect3dcryptosession9_getcertificatesize
ms.topic: method
f1_keywords: 
 - "d3d9/IDirect3DCryptoSession9.GetCertificateSize"
dev_langs:
 - c++
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
 - IDirect3DCryptoSession9.GetCertificateSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DCryptoSession9::GetCertificateSize


## -description


Gets the size of the driver's certificate chain.


## -parameters




### -param pCertificateSize

Receives the size of the certificate chain, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the certificate, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate">IDirect3DCryptoSession9::GetCertificate</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
 

 

