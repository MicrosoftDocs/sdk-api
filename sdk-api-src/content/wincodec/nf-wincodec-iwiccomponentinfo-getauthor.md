---
UID: NF:wincodec.IWICComponentInfo.GetAuthor
title: IWICComponentInfo::GetAuthor method
author: windows-driver-content
description: Retrieves the name of component's author.
old-location: wic\_wic_codec_iwiccomponentinfo_getauthor.htm
old-project: wic
ms.assetid: c92f707f-6077-4da0-9ac4-6d1f30fb5b75
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetAuthor method [Windows Imaging Component], GetAuthor method [Windows Imaging Component], IWICComponentInfo interface, GetAuthor,IWICComponentInfo.GetAuthor, IWICComponentInfo, IWICComponentInfo interface [Windows Imaging Component], GetAuthor method, IWICComponentInfo::GetAuthor, _wic_codec_iwiccomponentinfo_getauthor, wic._wic_codec_iwiccomponentinfo_getauthor, wincodec/IWICComponentInfo::GetAuthor
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
-	IWICComponentInfo.GetAuthor
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentInfo::GetAuthor method


## -description


Retrieves the name of component's author.


## -parameters




### -param cchAuthor [in]

Type: <b>UINT</b>

The size of the <i>wzAuthor</i> buffer.


### -param wzAuthor [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the name of the component's author.
               The locale of the string depends on the value that the codec wrote to the registry at install time. For built-in components, these strings are always in English.


### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's authors name. The author name is optional; if an author name is not specified by the component, the length returned is 0.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.



