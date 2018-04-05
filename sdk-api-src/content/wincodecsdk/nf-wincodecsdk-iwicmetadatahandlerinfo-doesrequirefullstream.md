---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.DoesRequireFullStream
title: IWICMetadataHandlerInfo::DoesRequireFullStream method
author: windows-driver-content
description: Determines if the handler requires a full stream.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream.htm
old-project: wic
ms.assetid: f434fd44-47a2-40be-ab3f-3d99b5e0e56a
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: DoesRequireFullStream method [Windows Imaging Component], DoesRequireFullStream method [Windows Imaging Component], IWICMetadataHandlerInfo interface, DoesRequireFullStream,IWICMetadataHandlerInfo.DoesRequireFullStream, IWICMetadataHandlerInfo, IWICMetadataHandlerInfo interface [Windows Imaging Component], DoesRequireFullStream method, IWICMetadataHandlerInfo::DoesRequireFullStream, _wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream, wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream, wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFullStream
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
-	IWICMetadataHandlerInfo.DoesRequireFullStream
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataHandlerInfo::DoesRequireFullStream method


## -description


Determines if the handler requires a full stream.


## -parameters




### -param pfRequiresFullStream [out]

Type: <b>BOOL*</b>

Pointer that receives <b>TRUE</b> if a full stream is required; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



