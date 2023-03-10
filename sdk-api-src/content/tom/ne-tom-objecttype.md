---
UID: NE:tom.__MIDL___MIDL_itf_tom_0000_0000_0002
title: OBJECTTYPE (tom.h)
description: Defines values that identify object types in the Text Object Model (TOM)  content.
helpviewer_keywords: ["OBJECTTYPE","OBJECTTYPE enumeration [Windows Controls]","controls.objecttype","tom/OBJECTTYPE","tom/tomAccent","tom/tomBox","tom/tomBoxedFormula","tom/tomBrackets","tom/tomBracketsWithSeps","tom/tomEq","tom/tomEquationArray","tom/tomFraction","tom/tomFunctionApply","tom/tomHorzVert","tom/tomLeftSubSup","tom/tomLowerLimit","tom/tomMath","tom/tomMatrix","tom/tomNary","tom/tomObjectMax","tom/tomOpChar","tom/tomOverbar","tom/tomPhantom","tom/tomRadical","tom/tomRuby","tom/tomSimpleText","tom/tomSlashedFraction","tom/tomStack","tom/tomStretchStack","tom/tomSubSup","tom/tomSubscript","tom/tomSuperscript","tom/tomUnderbar","tom/tomUpperLimit","tom/tomWarichu","tomAccent","tomBox","tomBoxedFormula","tomBrackets","tomBracketsWithSeps","tomEq","tomEquationArray","tomFraction","tomFunctionApply","tomHorzVert","tomLeftSubSup","tomLowerLimit","tomMath","tomMatrix","tomNary","tomObjectMax","tomOpChar","tomOverbar","tomPhantom","tomRadical","tomRuby","tomSimpleText","tomSlashedFraction","tomStack","tomStretchStack","tomSubSup","tomSubscript","tomSuperscript","tomUnderbar","tomUpperLimit","tomWarichu"]
old-location: controls\objecttype.htm
tech.root: Controls
ms.assetid: fbac082e-adf2-48f9-ae13-5ea1357fc428
ms.date: 12/05/2018
ms.keywords: OBJECTTYPE, OBJECTTYPE enumeration [Windows Controls], controls.objecttype, tom/OBJECTTYPE, tom/tomAccent, tom/tomBox, tom/tomBoxedFormula, tom/tomBrackets, tom/tomBracketsWithSeps, tom/tomEq, tom/tomEquationArray, tom/tomFraction, tom/tomFunctionApply, tom/tomHorzVert, tom/tomLeftSubSup, tom/tomLowerLimit, tom/tomMath, tom/tomMatrix, tom/tomNary, tom/tomObjectMax, tom/tomOpChar, tom/tomOverbar, tom/tomPhantom, tom/tomRadical, tom/tomRuby, tom/tomSimpleText, tom/tomSlashedFraction, tom/tomStack, tom/tomStretchStack, tom/tomSubSup, tom/tomSubscript, tom/tomSuperscript, tom/tomUnderbar, tom/tomUpperLimit, tom/tomWarichu, tomAccent, tomBox, tomBoxedFormula, tomBrackets, tomBracketsWithSeps, tomEq, tomEquationArray, tomFraction, tomFunctionApply, tomHorzVert, tomLeftSubSup, tomLowerLimit, tomMath, tomMatrix, tomNary, tomObjectMax, tomOpChar, tomOverbar, tomPhantom, tomRadical, tomRuby, tomSimpleText, tomSlashedFraction, tomStack, tomStretchStack, tomSubSup, tomSubscript, tomSuperscript, tomUnderbar, tomUpperLimit, tomWarichu
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OBJECTTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_tom_0000_0000_0002
 - tom/__MIDL___MIDL_itf_tom_0000_0000_0002
 - OBJECTTYPE
 - tom/OBJECTTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tom.h
api_name:
 - OBJECTTYPE
---

# OBJECTTYPE enumeration


## -description

Defines values that identify object types in the Text Object Model (TOM)  content.

## -enum-fields

### -field tomSimpleText:0

Not an inline function.

### -field tomRuby

Base text with ruby annotation.

### -field tomHorzVert

Text flows horizontally in a vertically oriented document.

### -field tomWarichu

A Warichu "2 lines in one" comment.

### -field tomEq:9

An RTF Eq (equation) field.

### -field tomMath:10

Math.

### -field tomAccent:tomMath

Accent (combining mark).

### -field tomBox

Abstract box with properties.

### -field tomBoxedFormula

Encloses the argument in a rectangle.

### -field tomBrackets

Encloses the argument in brackets, parentheses, and so on.

### -field tomBracketsWithSeps

Encloses the argument in brackets, parentheses, and so on, and with separators.

### -field tomEquationArray

Column of aligned equations.

### -field tomFraction

Fraction.

### -field tomFunctionApply

Function apply.

### -field tomLeftSubSup

Left subscript or superscript.

### -field tomLowerLimit

Second argument below the first.

### -field tomMatrix

Matrix.

### -field tomNary

General <i>n</i>-ary expression.

### -field tomOpChar

Internal use for no-build operators.

### -field tomOverbar

Overscores argument.

### -field tomPhantom

Special spacing.

### -field tomRadical

Square root, and so on.

### -field tomSlashedFraction

Skewed and built-up linear fractions.

### -field tomStack

"Fraction" with no divide bar.

### -field tomStretchStack

Stretch character horizontally over or under argument.

### -field tomSubscript

Subscript.

### -field tomSubSup

Subscript and superscript combination.

### -field tomSuperscript

Superscript.

### -field tomUnderbar

Underscores the argument.

### -field tomUpperLimit

Second argument above the first.

### -field tomObjectMax

The maximum value in the <a href="/windows/win32/api/tom/ne-tom-objecttype">OBJECTTYPE</a> enumeration.

