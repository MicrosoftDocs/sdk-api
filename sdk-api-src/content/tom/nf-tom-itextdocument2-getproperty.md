---
UID: NF:tom.ITextDocument2.GetProperty
title: ITextDocument2::GetProperty (tom.h)
description: Retrieves the value of a property.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Controls]","GetProperty method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetProperty method","ITextDocument2.GetProperty","ITextDocument2::GetProperty","controls.itextdocument2_getproperty","tom/ITextDocument2::GetProperty","tomCanCopy","tomCanRedo","tomCanUndo","tomDocMathBuild","tomEllipsisMode","tomEllipsisState","tomMathInterSpace","tomMathIntraSpace","tomMathLMargin","tomMathPostSpace","tomMathPreSpace","tomMathRMargin","tomMathWrapIndent","tomMathWrapRight","tomUndoLimit"]
old-location: controls\itextdocument2_getproperty.htm
tech.root: Controls
ms.assetid: 30775a51-0e63-453e-ac94-39d4510002f0
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetProperty method, ITextDocument2.GetProperty, ITextDocument2::GetProperty, controls.itextdocument2_getproperty, tom/ITextDocument2::GetProperty, tomCanCopy, tomCanRedo, tomCanUndo, tomDocMathBuild, tomEllipsisMode, tomEllipsisState, tomMathInterSpace, tomMathIntraSpace, tomMathLMargin, tomMathPostSpace, tomMathPreSpace, tomMathRMargin, tomMathWrapIndent, tomMathWrapRight, tomUndoLimit
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
 - ITextDocument2::GetProperty
 - tom/ITextDocument2::GetProperty
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
 - ITextDocument2.GetProperty
---

# ITextDocument2::GetProperty


## -description

Retrieves the value of a property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The identifier of the property to retrieve. It can be one of the following property IDs.

<a id="tomCanCopy_"></a>
<a id="tomcancopy_"></a>
<a id="TOMCANCOPY_"></a>


#### tomCanCopy

<a id="tomCanRedo_"></a>
<a id="tomcanredo_"></a>
<a id="TOMCANREDO_"></a>


#### tomCanRedo

<a id="tomCanUndo_"></a>
<a id="tomcanundo_"></a>
<a id="TOMCANUNDO_"></a>


#### tomCanUndo

<a id="tomDocMathBuild"></a>
<a id="tomdocmathbuild"></a>
<a id="TOMDOCMATHBUILD"></a>


#### tomDocMathBuild

<a id="tomMathInterSpace"></a>
<a id="tommathinterspace"></a>
<a id="TOMMATHINTERSPACE"></a>


#### tomMathInterSpace

<a id="tomMathIntraSpace"></a>
<a id="tommathintraspace"></a>
<a id="TOMMATHINTRASPACE"></a>


#### tomMathIntraSpace

<a id="tomMathLMargin"></a>
<a id="tommathlmargin"></a>
<a id="TOMMATHLMARGIN"></a>


#### tomMathLMargin

<a id="tomMathPostSpace"></a>
<a id="tommathpostspace"></a>
<a id="TOMMATHPOSTSPACE"></a>


#### tomMathPostSpace

<a id="tomMathPreSpace"></a>
<a id="tommathprespace"></a>
<a id="TOMMATHPRESPACE"></a>


#### tomMathPreSpace

<a id="tomMathRMargin_"></a>
<a id="tommathrmargin_"></a>
<a id="TOMMATHRMARGIN_"></a>


#### tomMathRMargin

<a id="tomMathWrapIndent"></a>
<a id="tommathwrapindent"></a>
<a id="TOMMATHWRAPINDENT"></a>


#### tomMathWrapIndent

<a id="tomMathWrapRight"></a>
<a id="tommathwrapright"></a>
<a id="TOMMATHWRAPRIGHT"></a>


#### tomMathWrapRight

<a id="tomUndoLimit"></a>
<a id="tomundolimit"></a>
<a id="TOMUNDOLIMIT"></a>


#### tomUndoLimit

<a id="tomEllipsisMode"></a>
<a id="tomellipsismode"></a>
<a id="TOMELLIPSISMODE"></a>


#### tomEllipsisMode

<a id="tomEllipsisState"></a>
<a id="tomellipsisstate"></a>
<a id="TOMELLIPSISSTATE"></a>


#### tomEllipsisState

### -param pValue [out]

Type: <b>long*</b>

The value of the property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getmathproperties">ITextDocument2::GetMathProperties</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-setproperty">ITextDocument2::SetProperty</a>