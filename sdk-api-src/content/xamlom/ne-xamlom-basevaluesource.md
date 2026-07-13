---
UID: NE:xamlom.BaseValueSource
title: BaseValueSource (xamlom.h)
description: Defines constants that specify where the effective value of a property was set.
helpviewer_keywords: ["Animation","BaseValueSource","BaseValueSource enumeration","BaseValueSourceBuiltInStyle","BaseValueSourceDefault","BaseValueSourceLocal","BaseValueSourceStyle","BaseValueSourceUnknown","BaseValueSourceVisualState","Coercion","DefaultStyleTrigger","ImplicitStyleReference","Inherited","ParentTemplate","ParentTemplateTrigger","StyleTrigger","TemplateTrigger","xaml_diagnostics.basevaluesource","xamlom/Animation","xamlom/BaseValueSource","xamlom/BaseValueSourceBuiltInStyle","xamlom/BaseValueSourceDefault","xamlom/BaseValueSourceLocal","xamlom/BaseValueSourceStyle","xamlom/BaseValueSourceUnknown","xamlom/BaseValueSourceVisualState","xamlom/Coercion","xamlom/DefaultStyleTrigger","xamlom/ImplicitStyleReference","xamlom/Inherited","xamlom/ParentTemplate","xamlom/ParentTemplateTrigger","xamlom/StyleTrigger","xamlom/TemplateTrigger"]
old-location: xaml_diagnostics\basevaluesource.htm
tech.root: xaml_diagnostics
ms.assetid: 1B5C4153-A266-43B1-B659-FE0FD0FD6A37
ms.date: 12/05/2018
ms.keywords: Animation, BaseValueSource, BaseValueSource enumeration, BaseValueSourceBuiltInStyle, BaseValueSourceDefault, BaseValueSourceLocal, BaseValueSourceStyle, BaseValueSourceUnknown, BaseValueSourceVisualState, Coercion, DefaultStyleTrigger, ImplicitStyleReference, Inherited, ParentTemplate, ParentTemplateTrigger, StyleTrigger, TemplateTrigger, xaml_diagnostics.basevaluesource, xamlom/Animation, xamlom/BaseValueSource, xamlom/BaseValueSourceBuiltInStyle, xamlom/BaseValueSourceDefault, xamlom/BaseValueSourceLocal, xamlom/BaseValueSourceStyle, xamlom/BaseValueSourceUnknown, xamlom/BaseValueSourceVisualState, xamlom/Coercion, xamlom/DefaultStyleTrigger, xamlom/ImplicitStyleReference, xamlom/Inherited, xamlom/ParentTemplate, xamlom/ParentTemplateTrigger, xamlom/StyleTrigger, xamlom/TemplateTrigger
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BaseValueSource
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BaseValueSource
 - xamlom/BaseValueSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - BaseValueSource
---

# BaseValueSource enumeration


## -description

Defines constants that specify where the effective value of a property was set.

## -enum-fields

### -field BaseValueSourceUnknown:0

The source of the property value is not known.

### -field BaseValueSourceDefault

The value has not been set locally or by any styles, so it has the
default value defined in generic.xaml.

### -field BaseValueSourceBuiltInStyle

The value was set by a built-in style.

### -field BaseValueSourceStyle

The value was set by a style.

### -field BaseValueSourceLocal

The value was set locally.

### -field Inherited

The value was inherited from a parent element.

### -field DefaultStyleTrigger

The value was set by a default style trigger.

### -field TemplateTrigger

The value was set by a template style.

### -field StyleTrigger

The value was set by a style trigger.

### -field ImplicitStyleReference

The value was set by an implicit style reference.

### -field ParentTemplate

The value was set by a parent template.

### -field ParentTemplateTrigger

The value was set by a parent template trigger.

### -field Animation

The value was set by an animation.

### -field Coercion

The value was coerced in code.

### -field BaseValueSourceVisualState

The value was set by a visual state. (Introduced in Windows 10, version 1607.)

