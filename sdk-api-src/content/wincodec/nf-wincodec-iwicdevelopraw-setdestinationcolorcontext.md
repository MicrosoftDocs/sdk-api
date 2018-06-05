---
UID: NF:wincodec.IWICDevelopRaw.SetDestinationColorContext
title: IWICDevelopRaw::SetDestinationColorContext
author: windows-sdk-content
description: Sets the destination color context.
old-location: wic\_wic_codec_iwicdevelopraw_setdestinationcolorcontext.htm
old-project: wic
ms.assetid: c5e82941-b52d-4f5b-8134-c3463464f1ac
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetDestinationColorContext method, IWICDevelopRaw.SetDestinationColorContext, IWICDevelopRaw::SetDestinationColorContext, SetDestinationColorContext, SetDestinationColorContext method [Windows Imaging Component], SetDestinationColorContext method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setdestinationcolorcontext, wic._wic_codec_iwicdevelopraw_setdestinationcolorcontext, wincodec/IWICDevelopRaw::SetDestinationColorContext
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw.SetDestinationColorContext
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetDestinationColorContext


## -description


Sets the destination color context.


## -parameters




### -param pColorContext [in]

Type: <b>const <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>*</b>

The destination color context.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



