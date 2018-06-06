---
UID: NF:wincodec.IWICColorContext.InitializeFromFilename
title: IWICColorContext::InitializeFromFilename
author: windows-sdk-content
description: Initializes the color context from the given file.
old-location: wic\_wic_codec_iwiccolorcontext_initializefromfilename.htm
old-project: wic
ms.assetid: df1f841b-6b01-42d5-967d-47ec402f9b8c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICColorContext interface [Windows Imaging Component],InitializeFromFilename method, IWICColorContext.InitializeFromFilename, IWICColorContext::InitializeFromFilename, InitializeFromFilename, InitializeFromFilename method [Windows Imaging Component], InitializeFromFilename method [Windows Imaging Component],IWICColorContext interface, _wic_codec_iwiccolorcontext_initializefromfilename, wic._wic_codec_iwiccolorcontext_initializefromfilename, wincodec/IWICColorContext::InitializeFromFilename
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICColorContext.InitializeFromFilename
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICColorContext::InitializeFromFilename


## -description


Initializes the color context from the given file.


## -parameters




### -param wzFilename [in]

Type: <b>LPCWSTR</b>

The name of the file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Once a color context has been initialized, it can't be re-initialized.





## -see-also




<a href="_color_GetColorDirectory">GetColorDirectory</a>



<a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>
 

 

