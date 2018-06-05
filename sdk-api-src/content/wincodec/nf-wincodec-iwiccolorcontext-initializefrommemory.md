---
UID: NF:wincodec.IWICColorContext.InitializeFromMemory
title: IWICColorContext::InitializeFromMemory
author: windows-sdk-content
description: Initializes the color context from a memory block.
old-location: wic\_wic_codec_iwiccolorcontext_initializefrommemory.htm
old-project: wic
ms.assetid: 0cadc79b-85d0-495e-8309-8d5e3b246242
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICColorContext interface [Windows Imaging Component],InitializeFromMemory method, IWICColorContext.InitializeFromMemory, IWICColorContext::InitializeFromMemory, InitializeFromMemory, InitializeFromMemory method [Windows Imaging Component], InitializeFromMemory method [Windows Imaging Component],IWICColorContext interface, _wic_codec_iwiccolorcontext_initializefrommemory, wic._wic_codec_iwiccolorcontext_initializefrommemory, wincodec/IWICColorContext::InitializeFromMemory
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
-	IWICColorContext.InitializeFromMemory
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICColorContext::InitializeFromMemory


## -description


Initializes the color context from a memory block.


## -parameters




### -param pbBuffer [in]

Type: <b>const BYTE*</b>

The buffer used to initialize the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.


### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the <i>pbBuffer</i> buffer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Once a color context has been initialized, it can't be re-initialized.




