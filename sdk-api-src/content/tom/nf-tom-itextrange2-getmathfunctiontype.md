---
UID: NF:tom.ITextRange2.GetMathFunctionType
title: ITextRange2::GetMathFunctionType (tom.h)
description: Retrieves the math function type associated with the specified math function name.
helpviewer_keywords: ["GetMathFunctionType","GetMathFunctionType method [Windows Controls]","GetMathFunctionType method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetMathFunctionType method","ITextRange2.GetMathFunctionType","ITextRange2::GetMathFunctionType","controls.itextrange2_getmathfunctiontype","tom/ITextRange2::GetMathFunctionType","tomFunctionTypeIsLim","tomFunctionTypeNone","tomFunctionTypeTakesArg","tomFunctionTypeTakesLim","tomFunctionTypeTakesLim2"]
old-location: controls\itextrange2_getmathfunctiontype.htm
tech.root: Controls
ms.assetid: 00bae237-5853-430e-8313-563da0cf0fde
ms.date: 12/05/2018
ms.keywords: GetMathFunctionType, GetMathFunctionType method [Windows Controls], GetMathFunctionType method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetMathFunctionType method, ITextRange2.GetMathFunctionType, ITextRange2::GetMathFunctionType, controls.itextrange2_getmathfunctiontype, tom/ITextRange2::GetMathFunctionType, tomFunctionTypeIsLim, tomFunctionTypeNone, tomFunctionTypeTakesArg, tomFunctionTypeTakesLim, tomFunctionTypeTakesLim2
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
 - ITextRange2::GetMathFunctionType
 - tom/ITextRange2::GetMathFunctionType
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
 - ITextRange2.GetMathFunctionType
---

# ITextRange2::GetMathFunctionType


## -description

Retrieves the math function type associated with the specified math function name.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

The math function name that is checked to determine the math function type.

### -param pValue [out]

Type: <b>long*</b>

The math function type of the function name specified by  <i>bstr</i>. It can be one of the following values.

<a id="tomFunctionTypeNone"></a>
<a id="tomfunctiontypenone"></a>
<a id="TOMFUNCTIONTYPENONE"></a>


#### tomFunctionTypeNone

<a id="tomFunctionTypeTakesArg"></a>
<a id="tomfunctiontypetakesarg"></a>
<a id="TOMFUNCTIONTYPETAKESARG"></a>


#### tomFunctionTypeTakesArg

<a id="tomFunctionTypeTakesLim"></a>
<a id="tomfunctiontypetakeslim"></a>
<a id="TOMFUNCTIONTYPETAKESLIM"></a>


#### tomFunctionTypeTakesLim

<a id="tomFunctionTypeTakesLim2"></a>
<a id="tomfunctiontypetakeslim2"></a>
<a id="TOMFUNCTIONTYPETAKESLIM2"></a>


#### tomFunctionTypeTakesLim2

<a id="tomFunctionTypeIsLim"></a>
<a id="tomfunctiontypeislim"></a>
<a id="TOMFUNCTIONTYPEISLIM"></a>


#### tomFunctionTypeIsLim

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>