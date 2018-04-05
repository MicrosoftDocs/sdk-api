---
UID: NF:wincodec.IWICImagingFactory.CreateComponentInfo
title: IWICImagingFactory::CreateComponentInfo method
author: windows-driver-content
description: Creates a new instance of the IWICComponentInfo class for the given component class identifier (CLSID).
old-location: wic\_wic_codec_iwicimagingfactory_createcomponentinfo.htm
old-project: wic
ms.assetid: c4feebf7-500f-4ab8-85fa-689edfe31846
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: CreateComponentInfo method [Windows Imaging Component], CreateComponentInfo method [Windows Imaging Component], IWICImagingFactory interface, CreateComponentInfo,IWICImagingFactory.CreateComponentInfo, IWICImagingFactory, IWICImagingFactory interface [Windows Imaging Component], CreateComponentInfo method, IWICImagingFactory::CreateComponentInfo, _wic_codec_iwicimagingfactory_createcomponentinfo, wic._wic_codec_iwicimagingfactory_createcomponentinfo, wincodec/IWICImagingFactory::CreateComponentInfo
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
-	IWICImagingFactory.CreateComponentInfo
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateComponentInfo method


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a> class for the given component class identifier (CLSID).


## -parameters




### -param clsidComponent [in]

Type: <b>REFCLSID</b>

The CLSID for the desired component.


### -param ppIInfo [out]

Type: <b><a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



