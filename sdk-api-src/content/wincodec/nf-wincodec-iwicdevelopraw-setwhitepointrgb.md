---
UID: NF:wincodec.IWICDevelopRaw.SetWhitePointRGB
title: IWICDevelopRaw::SetWhitePointRGB
author: windows-sdk-content
description: Sets the white point RGB values.
old-location: wic\_wic_codec_iwicdevelopraw_setwhitepointrgb.htm
tech.root: wic
ms.assetid: 7059959f-dcd6-46a6-a95c-1dd9610f865c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetWhitePointRGB method, IWICDevelopRaw.SetWhitePointRGB, IWICDevelopRaw::SetWhitePointRGB, SetWhitePointRGB, SetWhitePointRGB method [Windows Imaging Component], SetWhitePointRGB method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setwhitepointrgb, wic._wic_codec_iwicdevelopraw_setwhitepointrgb, wincodec/IWICDevelopRaw::SetWhitePointRGB
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.SetWhitePointRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICDevelopRaw.SetWhitePointRGB
: 
---

# IWICDevelopRaw::SetWhitePointRGB


## -description


Sets the white point RGB values.


## -parameters




### -param Red [in]

Type: <b>UINT</b>

The red white point value.


### -param Green [in]

Type: <b>UINT</b>

The green white point value.


### -param Blue [in]

Type: <b>UINT</b>

The blue white point value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Due to other white point setting methods (e.g. <a href="https://msdn.microsoft.com/3a5235ed-b0c8-4090-9380-892e3e994d10">SetWhitePointKelvin</a>), care must be taken by codec implementers to ensure proper interoperability. For instance, if the caller sets via a named white point then the codec implementer may whis to disable reading back the correspoinding Kelvin temperature. In specific cases where the codec implementer wishes to deny a given action because of previous calls, <b>WINCODEC_ERR_WRONGSTATE</b> should be returned.



