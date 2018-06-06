---
UID: NF:wincodec.IWICDevelopRaw.GetRotation
title: IWICDevelopRaw::GetRotation
author: windows-sdk-content
description: Gets the current rotation angle.
old-location: wic\_wic_codec_iwicdevelopraw_getrotation.htm
old-project: wic
ms.assetid: 671bca6d-bbe5-4f07-9735-12d796013d9e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetRotation, GetRotation method [Windows Imaging Component], GetRotation method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetRotation method, IWICDevelopRaw.GetRotation, IWICDevelopRaw::GetRotation, _wic_codec_iwicdevelopraw_getrotation, wic._wic_codec_iwicdevelopraw_getrotation, wincodec/IWICDevelopRaw::GetRotation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.GetRotation
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::GetRotation


## -description


Gets the current rotation angle.


## -parameters




### -param pRotation [out]

Type: <b>double*</b>

A pointer that receives the current rotation angle.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



