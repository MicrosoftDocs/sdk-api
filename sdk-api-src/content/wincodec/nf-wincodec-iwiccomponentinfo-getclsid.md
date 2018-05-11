---
UID: NF:wincodec.IWICComponentInfo.GetCLSID
title: IWICComponentInfo::GetCLSID
author: windows-driver-content
description: Retrieves the component's class identifier (CLSID)
old-location: wic\_wic_codec_iwiccomponentinfo_getclsid.htm
old-project: wic
ms.assetid: 63814933-1366-47b9-8cf4-0d8685053a30
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetCLSID, GetCLSID method [Windows Imaging Component], GetCLSID method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetCLSID method, IWICComponentInfo.GetCLSID, IWICComponentInfo::GetCLSID, _wic_codec_iwiccomponentinfo_getclsid, wic._wic_codec_iwiccomponentinfo_getclsid, wincodec/IWICComponentInfo::GetCLSID
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
-	Windowscodecs.dll
api_name:
-	IWICComponentInfo.GetCLSID
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



