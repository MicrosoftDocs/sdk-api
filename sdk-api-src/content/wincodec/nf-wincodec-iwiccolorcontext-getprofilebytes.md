---
UID: NF:wincodec.IWICColorContext.GetProfileBytes
title: IWICColorContext::GetProfileBytes (wincodec.h)
author: windows-sdk-content
description: Retrieves the color context profile.
old-location: wic\_wic_codec_iwiccolorcontext_getprofilebytes.htm
tech.root: wic
ms.assetid: 59427a49-ef68-4680-b6d8-4ffa2a1913b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProfileBytes, GetProfileBytes method [Windows Imaging Component], GetProfileBytes method [Windows Imaging Component],IWICColorContext interface, IWICColorContext interface [Windows Imaging Component],GetProfileBytes method, IWICColorContext.GetProfileBytes, IWICColorContext::GetProfileBytes, _wic_codec_iwiccolorcontext_getprofilebytes, wic._wic_codec_iwiccolorcontext_getprofilebytes, wincodec/IWICColorContext::GetProfileBytes
ms.topic: method
f1_keywords: 
 - "wincodec/IWICColorContext.GetProfileBytes"
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
 - IWICColorContext.GetProfileBytes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICColorContext::GetProfileBytes


## -description


Retrieves the color context profile.


## -parameters




### -param cbBuffer [in]

Type: <b>UINT</b>

The size of the <i>pbBuffer</i> buffer.


### -param pbBuffer [in, out]

Type: <b>BYTE*</b>

A pointer that receives the color context profile.


### -param pcbActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual buffer size needed to retrieve the entire color context profile.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only use this method if the context type is <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextProfile</a>.


Calling this method with <i>pbBuffer</i> set to <b>NULL</b> will cause it to return the required buffer size in <i>pcbActual</i>.




