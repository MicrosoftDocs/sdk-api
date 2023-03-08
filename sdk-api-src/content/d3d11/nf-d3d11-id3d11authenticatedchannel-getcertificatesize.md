---
UID: NF:d3d11.ID3D11AuthenticatedChannel.GetCertificateSize
title: ID3D11AuthenticatedChannel::GetCertificateSize (d3d11.h)
description: Gets the size of the driver's certificate chain. (ID3D11AuthenticatedChannel.GetCertificateSize)
helpviewer_keywords: ["GetCertificateSize","GetCertificateSize method [Media Foundation]","GetCertificateSize method [Media Foundation]","ID3D11AuthenticatedChannel interface","ID3D11AuthenticatedChannel interface [Media Foundation]","GetCertificateSize method","ID3D11AuthenticatedChannel.GetCertificateSize","ID3D11AuthenticatedChannel::GetCertificateSize","d3d11/ID3D11AuthenticatedChannel::GetCertificateSize","mf.id3d11authenticatedchannel_getcertificatesize"]
old-location: mf\id3d11authenticatedchannel_getcertificatesize.htm
tech.root: mf
ms.assetid: B393140A-9744-4290-B168-4E7F4E9F55DC
ms.date: 12/05/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],ID3D11AuthenticatedChannel interface, ID3D11AuthenticatedChannel interface [Media Foundation],GetCertificateSize method, ID3D11AuthenticatedChannel.GetCertificateSize, ID3D11AuthenticatedChannel::GetCertificateSize, d3d11/ID3D11AuthenticatedChannel::GetCertificateSize, mf.id3d11authenticatedchannel_getcertificatesize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11AuthenticatedChannel::GetCertificateSize
 - d3d11/ID3D11AuthenticatedChannel::GetCertificateSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11AuthenticatedChannel.GetCertificateSize
---

# ID3D11AuthenticatedChannel::GetCertificateSize


## -description

Gets the size of the driver's certificate chain.

## -parameters

### -param pCertificateSize [out]

Receives the size of the certificate chain, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/getcertificatesize">GetCertificateSize</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a>
