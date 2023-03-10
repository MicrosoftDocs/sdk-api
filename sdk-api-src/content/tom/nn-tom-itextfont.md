---
UID: NN:tom.ITextFont
title: ITextFont (tom.h)
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara. (ITextFont)
helpviewer_keywords: ["ITextFont","ITextFont interface [Windows Controls]","ITextFont interface [Windows Controls]","described","_win32_ITextFont","_win32_ITextFont_cpp","controls.ITextFont","controls._win32_ITextFont","tom/ITextFont"]
old-location: controls\ITextFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont.htm
ms.date: 12/05/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], ITextFont interface [Windows Controls],described, _win32_ITextFont, _win32_ITextFont_cpp, controls.ITextFont, controls._win32_ITextFont, tom/ITextFont
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
 - ITextFont
 - tom/ITextFont
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
 - ITextFont
---

# ITextFont interface


## -description

Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <b>ITextFont</b> and <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>.

## -inheritance

The <b>ITextFont</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextFont</b> also has these types of members:

## -remarks

The <b>ITextFont</b> and <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.


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

The <b>ITextFont</b> attribute interface represents the traditional Microsoft Visual Basic for Applications (VBA) way of setting properties and it gives the desired VBA notation.

<b>ITextFont</b> uses the "tomBool" type for rich-text attributes that have binary states. For more information, see <a href="/windows/desktop/Controls/about-text-object-model">The tomBool Type</a>.

The rich edit control is able to accept and return all <b>ITextFont</b> properties intact, that is, without modification, both through TOM and through its Rich Text Format (RTF) converters. However, it cannot display the All Caps, Animation, Embossed, Imprint, Shadow, Small Caps, Hidden, Kerning, Outline, and Style font properties.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
