---
UID: NF:tom.ITextFont2.SetCompressionMode
title: ITextFont2::SetCompressionMode (tom.h)
description: Sets the East Asian compression mode.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetCompressionMode method","ITextFont2.SetCompressionMode","ITextFont2::SetCompressionMode","SetCompressionMode","SetCompressionMode method [Windows Controls]","SetCompressionMode method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setcompressionmode","tom/ITextFont2::SetCompressionMode","tomCompressNone (default)","tomCompressPunctuation","tomCompressPunctuationAndKana"]
old-location: controls\itextfont2_setcompressionmode.htm
tech.root: Controls
ms.assetid: 834bb793-b4a8-40b6-b210-05d17332ddb8
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetCompressionMode method, ITextFont2.SetCompressionMode, ITextFont2::SetCompressionMode, SetCompressionMode, SetCompressionMode method [Windows Controls], SetCompressionMode method [Windows Controls],ITextFont2 interface, controls.itextfont2_setcompressionmode, tom/ITextFont2::SetCompressionMode, tomCompressNone (default), tomCompressPunctuation, tomCompressPunctuationAndKana
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont2::SetCompressionMode
 - tom/ITextFont2::SetCompressionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.SetCompressionMode
---

# ITextFont2::SetCompressionMode


## -description

Sets the East Asian compression mode.

## -parameters

### -param Value [in]

Type: <b>long</b>


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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getcompressionmode">ITextFont2::GetCompressionMode</a>