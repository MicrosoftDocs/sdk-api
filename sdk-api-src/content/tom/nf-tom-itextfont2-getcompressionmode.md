---
UID: NF:tom.ITextFont2.GetCompressionMode
title: ITextFont2::GetCompressionMode
author: windows-sdk-content
description: Gets the East Asian compression mode.
old-location: controls\itextfont2_getcompressionmode.htm
tech.root: controls
ms.assetid: 3fefba0c-54a3-4013-8922-ba556ef785a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCompressionMode, GetCompressionMode method [Windows Controls], GetCompressionMode method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetCompressionMode method, ITextFont2.GetCompressionMode, ITextFont2::GetCompressionMode, controls.itextfont2_getcompressionmode, tom/ITextFont2::GetCompressionMode, tomCompressNone (default), tomCompressPunctuation, tomCompressPunctuationAndKana
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.GetCompressionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::GetCompressionMode


## -description


Gets the East Asian compression mode.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>


The compression mode, which can be one of these values:



<a id="tomCompressNone__default_"></a>
<a id="tomcompressnone__default_"></a>
<a id="TOMCOMPRESSNONE__DEFAULT_"></a>


#### tomCompressNone (default)

<a id="tomCompressPunctuation"></a>
<a id="tomcompresspunctuation"></a>
<a id="TOMCOMPRESSPUNCTUATION"></a>


#### tomCompressPunctuation

<a id="tomCompressPunctuationAndKana"></a>
<a id="tomcompresspunctuationandkana"></a>
<a id="TOMCOMPRESSPUNCTUATIONANDKANA"></a>


#### tomCompressPunctuationAndKana


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/834bb793-b4a8-40b6-b210-05d17332ddb8">ITextFont2::SetCompressionMode</a>
 

 

