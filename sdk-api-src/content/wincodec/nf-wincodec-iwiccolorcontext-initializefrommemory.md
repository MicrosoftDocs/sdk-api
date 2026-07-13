---
UID: NF:wincodec.IWICColorContext.InitializeFromMemory
title: IWICColorContext::InitializeFromMemory (wincodec.h)
description: Initializes the color context from a memory block.
helpviewer_keywords: ["IWICColorContext interface [Windows Imaging Component]","InitializeFromMemory method","IWICColorContext.InitializeFromMemory","IWICColorContext::InitializeFromMemory","InitializeFromMemory","InitializeFromMemory method [Windows Imaging Component]","InitializeFromMemory method [Windows Imaging Component]","IWICColorContext interface","_wic_codec_iwiccolorcontext_initializefrommemory","wic._wic_codec_iwiccolorcontext_initializefrommemory","wincodec/IWICColorContext::InitializeFromMemory"]
old-location: wic\_wic_codec_iwiccolorcontext_initializefrommemory.htm
tech.root: wic
ms.assetid: 0cadc79b-85d0-495e-8309-8d5e3b246242
ms.date: 12/05/2018
ms.keywords: IWICColorContext interface [Windows Imaging Component],InitializeFromMemory method, IWICColorContext.InitializeFromMemory, IWICColorContext::InitializeFromMemory, InitializeFromMemory, InitializeFromMemory method [Windows Imaging Component], InitializeFromMemory method [Windows Imaging Component],IWICColorContext interface, _wic_codec_iwiccolorcontext_initializefrommemory, wic._wic_codec_iwiccolorcontext_initializefrommemory, wincodec/IWICColorContext::InitializeFromMemory
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
 - IWICColorContext::InitializeFromMemory
 - wincodec/IWICColorContext::InitializeFromMemory
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
 - IWICColorContext.InitializeFromMemory
---

# IWICColorContext::InitializeFromMemory


## -description

Initializes the color context from a memory block.

## -parameters

### -param pbBuffer [in]

Type: <b>const BYTE*</b>

The buffer used to initialize the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.

### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the <i>pbBuffer</i> buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Once a color context has been initialized, it can't be re-initialized.