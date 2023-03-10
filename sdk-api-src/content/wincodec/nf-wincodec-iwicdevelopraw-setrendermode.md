---
UID: NF:wincodec.IWICDevelopRaw.SetRenderMode
title: IWICDevelopRaw::SetRenderMode (wincodec.h)
description: Sets the current WICRawRenderMode.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetRenderMode method","IWICDevelopRaw.SetRenderMode","IWICDevelopRaw::SetRenderMode","SetRenderMode","SetRenderMode method [Windows Imaging Component]","SetRenderMode method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setrendermode","wic._wic_codec_iwicdevelopraw_setrendermode","wincodec/IWICDevelopRaw::SetRenderMode"]
old-location: wic\_wic_codec_iwicdevelopraw_setrendermode.htm
tech.root: wic
ms.assetid: 3150abb3-795d-416d-b3eb-0001796f510d
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetRenderMode method, IWICDevelopRaw.SetRenderMode, IWICDevelopRaw::SetRenderMode, SetRenderMode, SetRenderMode method [Windows Imaging Component], SetRenderMode method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setrendermode, wic._wic_codec_iwicdevelopraw_setrendermode, wincodec/IWICDevelopRaw::SetRenderMode
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICDevelopRaw::SetRenderMode
 - wincodec/IWICDevelopRaw::SetRenderMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.SetRenderMode
---

# IWICDevelopRaw::SetRenderMode


## -description

Sets the current <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawrendermode">WICRawRenderMode</a>.

## -parameters

### -param RenderMode [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawrendermode">WICRawRenderMode</a></b>

The render mode to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.