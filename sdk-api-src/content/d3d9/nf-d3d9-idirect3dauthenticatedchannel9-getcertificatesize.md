---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.GetCertificateSize
title: IDirect3DAuthenticatedChannel9::GetCertificateSize
author: windows-sdk-content
description: Gets the size of the driver's certificate chain.
old-location: mf\idirect3dauthenticatedchannel9_getcertificatesize.htm
old-project: medfound
ms.assetid: a320a7be-6a0f-4de1-afc2-11eb2d7c24d6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],GetCertificateSize method, IDirect3DAuthenticatedChannel9.GetCertificateSize, IDirect3DAuthenticatedChannel9::GetCertificateSize, d3d9/IDirect3DAuthenticatedChannel9::GetCertificateSize, mf.idirect3dauthenticatedchannel9_getcertificatesize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DAuthenticatedChannel9.GetCertificateSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirect3DAuthenticatedChannel9::GetCertificateSize


## -description


Gets the size of the driver's certificate chain.


## -parameters




### -param pCertificateSize

Receives the size of the certificate chain, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the certificate chain, call <a href="https://msdn.microsoft.com/0663d3a0-256b-4c96-aca7-06c4d1853554">IDirect3DAuthenticatedChannel9::GetCertificate</a>.

This method fails if the channel type is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, because the Direct3D 9 channel does not support authentication.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
 

 

