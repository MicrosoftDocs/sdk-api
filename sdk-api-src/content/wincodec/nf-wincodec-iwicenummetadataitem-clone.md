---
UID: NF:wincodec.IWICEnumMetadataItem.Clone
title: IWICEnumMetadataItem::Clone (wincodec.h)
description: Creates a copy of the current IWICEnumMetadataItem.
helpviewer_keywords: ["Clone","Clone method [Windows Imaging Component]","Clone method [Windows Imaging Component]","IWICEnumMetadataItem interface","IWICEnumMetadataItem interface [Windows Imaging Component]","Clone method","IWICEnumMetadataItem.Clone","IWICEnumMetadataItem::Clone","_wic_codec_iwicenummetadataitem_clone","wic._wic_codec_iwicenummetadataitem_clone","wincodec/IWICEnumMetadataItem::Clone"]
old-location: wic\_wic_codec_iwicenummetadataitem_clone.htm
tech.root: wic
ms.assetid: 08477910-027e-497d-a3e7-16e92f1a53e9
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Imaging Component], Clone method [Windows Imaging Component],IWICEnumMetadataItem interface, IWICEnumMetadataItem interface [Windows Imaging Component],Clone method, IWICEnumMetadataItem.Clone, IWICEnumMetadataItem::Clone, _wic_codec_iwicenummetadataitem_clone, wic._wic_codec_iwicenummetadataitem_clone, wincodec/IWICEnumMetadataItem::Clone
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICEnumMetadataItem::Clone
 - wincodec/IWICEnumMetadataItem::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICEnumMetadataItem.Clone
---

# IWICEnumMetadataItem::Clone


## -description

Creates a copy of the current <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicenummetadataitem">IWICEnumMetadataItem</a>.

## -parameters

### -param ppIEnumMetadataItem [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicenummetadataitem">IWICEnumMetadataItem</a>**</b>

A pointer that receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicenummetadataitem">IWICEnumMetadataItem</a> copy.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.