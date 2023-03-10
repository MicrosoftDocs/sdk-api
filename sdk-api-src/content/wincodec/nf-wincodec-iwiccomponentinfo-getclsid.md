---
UID: NF:wincodec.IWICComponentInfo.GetCLSID
title: IWICComponentInfo::GetCLSID (wincodec.h)
description: Retrieves the component's class identifier (CLSID)
helpviewer_keywords: ["GetCLSID","GetCLSID method [Windows Imaging Component]","GetCLSID method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetCLSID method","IWICComponentInfo.GetCLSID","IWICComponentInfo::GetCLSID","_wic_codec_iwiccomponentinfo_getclsid","wic._wic_codec_iwiccomponentinfo_getclsid","wincodec/IWICComponentInfo::GetCLSID"]
old-location: wic\_wic_codec_iwiccomponentinfo_getclsid.htm
tech.root: wic
ms.assetid: 63814933-1366-47b9-8cf4-0d8685053a30
ms.date: 12/05/2018
ms.keywords: GetCLSID, GetCLSID method [Windows Imaging Component], GetCLSID method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetCLSID method, IWICComponentInfo.GetCLSID, IWICComponentInfo::GetCLSID, _wic_codec_iwiccomponentinfo_getclsid, wic._wic_codec_iwiccomponentinfo_getclsid, wincodec/IWICComponentInfo::GetCLSID
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
 - IWICComponentInfo::GetCLSID
 - wincodec/IWICComponentInfo::GetCLSID
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
 - IWICComponentInfo.GetCLSID
---

# IWICComponentInfo::GetCLSID


## -description

Retrieves the component's class identifier (CLSID)

## -parameters

### -param pclsid [out]

Type: <b>CLSID*</b>

A pointer that receives the component's CLSID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

