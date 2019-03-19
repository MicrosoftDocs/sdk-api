---
UID: NF:wincodec.IWICEnumMetadataItem.Clone
title: IWICEnumMetadataItem::Clone (wincodec.h)
author: windows-sdk-content
description: Creates a copy of the current IWICEnumMetadataItem.
old-location: wic\_wic_codec_iwicenummetadataitem_clone.htm
tech.root: wic
ms.assetid: 08477910-027e-497d-a3e7-16e92f1a53e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Windows Imaging Component], Clone method [Windows Imaging Component],IWICEnumMetadataItem interface, IWICEnumMetadataItem interface [Windows Imaging Component],Clone method, IWICEnumMetadataItem.Clone, IWICEnumMetadataItem::Clone, _wic_codec_iwicenummetadataitem_clone, wic._wic_codec_iwicenummetadataitem_clone, wincodec/IWICEnumMetadataItem::Clone
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICEnumMetadataItem.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICEnumMetadataItem::Clone


## -description


Creates a copy of the current <a href="https://msdn.microsoft.com/4fe0e47f-9ef4-4aa1-a3ae-578b3759f9ef">IWICEnumMetadataItem</a>.


## -parameters




### -param ppIEnumMetadataItem [out]

Type: <b><a href="https://msdn.microsoft.com/4fe0e47f-9ef4-4aa1-a3ae-578b3759f9ef">IWICEnumMetadataItem</a>**</b>

A pointer that receives a pointer to the <a href="https://msdn.microsoft.com/4fe0e47f-9ef4-4aa1-a3ae-578b3759f9ef">IWICEnumMetadataItem</a> copy.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



