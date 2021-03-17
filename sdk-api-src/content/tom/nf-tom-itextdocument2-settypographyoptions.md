---
UID: NF:tom.ITextDocument2.SetTypographyOptions
title: ITextDocument2::SetTypographyOptions (tom.h)
description: Specifies the typography options for the document.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetTypographyOptions method","ITextDocument2.SetTypographyOptions","ITextDocument2::SetTypographyOptions","SetTypographyOptions","SetTypographyOptions method [Windows Controls]","SetTypographyOptions method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_settypographyoptions","tom/ITextDocument2::SetTypographyOptions"]
old-location: controls\itextdocument2_settypographyoptions.htm
tech.root: Controls
ms.assetid: 1013c9bf-b6fe-4396-b7a8-36e61edf1df3
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetTypographyOptions method, ITextDocument2.SetTypographyOptions, ITextDocument2::SetTypographyOptions, SetTypographyOptions, SetTypographyOptions method [Windows Controls], SetTypographyOptions method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_settypographyoptions, tom/ITextDocument2::SetTypographyOptions
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
 - ITextDocument2::SetTypographyOptions
 - tom/ITextDocument2::SetTypographyOptions
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
 - ITextDocument2.SetTypographyOptions
---

# ITextDocument2::SetTypographyOptions


## -description

Specifies the typography options for the document.

## -parameters

### -param Options [in]

Type: <b>long</b>

The typography options to set. For a list of possible options, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-gettypographyoptions">GetTypographyOptions</a>.

### -param Mask [in]

Type: <b>long</b>

A mask identifying the options to set. For example, to turn on <b>TO_ADVANCEDTYPOGRAPHY</b>, call <b>ITextDocument2::SetTypographyOptions (TO_ADVANCEDTYPOGRAPHY, TO_ADVANCEDTYPOGRAPHY)</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-gettypographyoptions">ITextDocument2::GetTypographyOptions</a>