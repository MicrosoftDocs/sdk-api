---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.DoesRequireFixedSize
title: IWICMetadataHandlerInfo::DoesRequireFixedSize
author: windows-driver-content
description: Determines if the metadata handler requires a fixed size.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize.htm
old-project: wic
ms.assetid: 522294c5-e424-40cf-b982-275198e705dc
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: DoesRequireFixedSize, DoesRequireFixedSize method [Windows Imaging Component], DoesRequireFixedSize method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],DoesRequireFixedSize method, IWICMetadataHandlerInfo.DoesRequireFixedSize, IWICMetadataHandlerInfo::DoesRequireFixedSize, _wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize, wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize, wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFixedSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICMetadataHandlerInfo.DoesRequireFixedSize
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataHandlerInfo::DoesRequireFixedSize


## -description


Determines if the metadata handler requires a fixed size.


## -parameters




### -param pfFixedSize [out]

Type: <b>BOOL*</b>

Pointer that receives <b>TRUE</b> if a fixed size is required; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



