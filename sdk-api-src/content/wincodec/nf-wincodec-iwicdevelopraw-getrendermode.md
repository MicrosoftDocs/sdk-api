---
UID: NF:wincodec.IWICDevelopRaw.GetRenderMode
title: IWICDevelopRaw::GetRenderMode
author: windows-sdk-content
description: Gets the current WICRawRenderMode.
old-location: wic\_wic_codec_iwicdevelopraw_getrendermode.htm
old-project: wic
ms.assetid: d8cf4508-6a2c-4d02-b98f-0455a3dc966c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRenderMode, GetRenderMode method [Windows Imaging Component], GetRenderMode method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetRenderMode method, IWICDevelopRaw.GetRenderMode, IWICDevelopRaw::GetRenderMode, _wic_codec_iwicdevelopraw_getrendermode, wic._wic_codec_iwicdevelopraw_getrendermode, wincodec/IWICDevelopRaw::GetRenderMode
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICDevelopRaw.GetRenderMode
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::GetRenderMode


## -description


Gets the current <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>.


## -parameters




### -param pRenderMode [out]

Type: <b><a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>*</b>

A pointer that receives the current <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



