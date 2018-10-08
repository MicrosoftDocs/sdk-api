---
UID: NF:d3d9.IDirect3DCryptoSession9.GetCertificateSize
title: IDirect3DCryptoSession9::GetCertificateSize
author: windows-sdk-content
description: Gets the size of the driver's certificate chain.
old-location: mf\idirect3dcryptosession9_getcertificatesize.htm
tech.root: medfound
ms.assetid: f85f3453-5bf8-412c-9ed9-e39bff496df6
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetCertificateSize method, IDirect3DCryptoSession9.GetCertificateSize, IDirect3DCryptoSession9::GetCertificateSize, d3d9/IDirect3DCryptoSession9::GetCertificateSize, mf.idirect3dcryptosession9_getcertificatesize
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
 - IDirect3DCryptoSession9.GetCertificateSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



To get the certificate, call <a href="https://msdn.microsoft.com/802285a6-1338-4131-bb5e-9d4daad62bdc">IDirect3DCryptoSession9::GetCertificate</a>.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 

