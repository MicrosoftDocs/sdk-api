---
UID: NF:wincodec.IWICDevelopRaw.SetRenderMode
title: IWICDevelopRaw::SetRenderMode method
author: windows-driver-content
description: Sets the current WICRawRenderMode.
old-location: wic\_wic_codec_iwicdevelopraw_setrendermode.htm
old-project: wic
ms.assetid: 3150abb3-795d-416d-b3eb-0001796f510d
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICDevelopRaw, IWICDevelopRaw interface [Windows Imaging Component], SetRenderMode method, IWICDevelopRaw::SetRenderMode, SetRenderMode method [Windows Imaging Component], SetRenderMode method [Windows Imaging Component], IWICDevelopRaw interface, SetRenderMode,IWICDevelopRaw.SetRenderMode, _wic_codec_iwicdevelopraw_setrendermode, wic._wic_codec_iwicdevelopraw_setrendermode, wincodec/IWICDevelopRaw::SetRenderMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.lib
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw.SetRenderMode
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetRenderMode method


## -description


Sets the current <a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a>.


## -parameters




### -param RenderMode [in]

Type: <b><a href="https://msdn.microsoft.com/dc020c78-a018-42ee-a500-65a743b96107">WICRawRenderMode</a></b>

The render mode to use.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



