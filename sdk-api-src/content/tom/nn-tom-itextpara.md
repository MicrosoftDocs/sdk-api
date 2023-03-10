---
UID: NN:tom.ITextPara
title: ITextPara (tom.h)
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara. (ITextPara)
helpviewer_keywords: ["ITextPara","ITextPara interface [Windows Controls]","ITextPara interface [Windows Controls]","described","_win32_ITextPara","_win32_ITextPara_cpp","controls.ITextPara","controls._win32_ITextPara","tom/ITextPara"]
old-location: controls\ITextPara.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara.htm
ms.date: 12/05/2018
ms.keywords: ITextPara, ITextPara interface [Windows Controls], ITextPara interface [Windows Controls],described, _win32_ITextPara, _win32_ITextPara_cpp, controls.ITextPara, controls._win32_ITextPara, tom/ITextPara
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextPara
 - tom/ITextPara
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
 - ITextPara
---

# ITextPara interface


## -description

Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <b>ITextPara</b>.

## -inheritance

The <b>ITextPara</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextPara</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <b>ITextPara</b> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.


```
Sub AttributeCopy(r1 As ITextRange, r2 As ITextRange)
    Dim tf As ITextFont
    tf = r1.Font                ' Value is the default property    
    tf.Bold = tomTrue           ' You can make some modifications
    tf.Size = 12
    tf.Animation = tomSparkleText
    r2.Font = tf                ' Apply font attributes all at once
End Sub
```


See <a href="/windows/desktop/api/tom/nf-tom-itextrange-setfont">SetFont</a> for a similar example written in C++.

The <b>ITextPara</b> interface encapsulates the Word Paragraph dialog box. All measurements are given in floating-point points. The rich edit control is able to accept and return all <b>ITextPara</b> properties intact (that is, without modification), both through TOM and through its Rich Text Format (RTF) converters. However, the following properties have no effect on what the control displays:

<ul>
<li>DoNotHyphen</li>
<li>KeepTogether</li>
<li>KeepWithNext</li>
<li>LineSpacing</li>
<li>LineSpacingRule</li>
<li>NoLineNumber</li>
<li>PageBreakBefore</li>
<li>Tab alignments</li>
<li>Tab styles (other than tomAlignLeft and tomSpaces)</li>
<li>Style WidowControl</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
