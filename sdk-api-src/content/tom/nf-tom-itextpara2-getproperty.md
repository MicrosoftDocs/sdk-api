---
UID: NF:tom.ITextPara2.GetProperty
title: ITextPara2::GetProperty (tom.h)
description: Gets the value of the specified property. (ITextPara2.GetProperty)
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Controls]","GetProperty method [Windows Controls]","ITextPara2 interface","ITextPara2 interface [Windows Controls]","GetProperty method","ITextPara2.GetProperty","ITextPara2::GetProperty","controls.itextpara2_getproperty","tom/ITextPara2::GetProperty"]
old-location: controls\itextpara2_getproperty.htm
tech.root: Controls
ms.assetid: 628ec2d7-2553-4a76-a5e6-c3a5bef3f8d6
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetProperty method, ITextPara2.GetProperty, ITextPara2::GetProperty, controls.itextpara2_getproperty, tom/ITextPara2::GetProperty
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
 - ITextPara2::GetProperty
 - tom/ITextPara2::GetProperty
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
 - ITextPara2.GetProperty
---

# ITextPara2::GetProperty


## -description

Gets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The ID of the property value to retrieve.

### -param pValue [out]

Type: <b>long*</b>

The property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/win32/api/tom/ne-tom-tomconstants">tomParaPropMathAlign</a> property sets the math alignment for math paragraphs in a text paragraph. It can have one of the following values.<dl>
<dd><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathParaAlignDefault</a></dd>
<dd><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathParaAlignCenterGroup</a></dd>
<dd><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathParaAlignCenter</a></dd>
<dd><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathParaAlignLeft</a></dd>
<dd><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomMathParaAlignRight</a></dd>
</dl>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-setproperty">ITextPara2::SetProperty</a>
