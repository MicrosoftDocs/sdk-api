---
UID: NF:wincodec.IWICDevelopRaw.SetDestinationColorContext
title: IWICDevelopRaw::SetDestinationColorContext (wincodec.h)
description: Sets the destination color context.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetDestinationColorContext method","IWICDevelopRaw.SetDestinationColorContext","IWICDevelopRaw::SetDestinationColorContext","SetDestinationColorContext","SetDestinationColorContext method [Windows Imaging Component]","SetDestinationColorContext method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setdestinationcolorcontext","wic._wic_codec_iwicdevelopraw_setdestinationcolorcontext","wincodec/IWICDevelopRaw::SetDestinationColorContext"]
old-location: wic\_wic_codec_iwicdevelopraw_setdestinationcolorcontext.htm
tech.root: wic
ms.assetid: c5e82941-b52d-4f5b-8134-c3463464f1ac
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetDestinationColorContext method, IWICDevelopRaw.SetDestinationColorContext, IWICDevelopRaw::SetDestinationColorContext, SetDestinationColorContext, SetDestinationColorContext method [Windows Imaging Component], SetDestinationColorContext method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setdestinationcolorcontext, wic._wic_codec_iwicdevelopraw_setdestinationcolorcontext, wincodec/IWICDevelopRaw::SetDestinationColorContext
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
 - IWICDevelopRaw::SetDestinationColorContext
 - wincodec/IWICDevelopRaw::SetDestinationColorContext
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
 - IWICDevelopRaw.SetDestinationColorContext
---

# IWICDevelopRaw::SetDestinationColorContext


## -description

Sets the destination color context.

## -parameters

### -param pColorContext [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>*</b>

The destination color context.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.