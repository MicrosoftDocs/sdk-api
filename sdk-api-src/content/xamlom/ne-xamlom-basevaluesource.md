---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# BaseValueSource enumeration


## -description


Defines constants that specify where the effective value of a property was set.


## -enum-fields




### -field BaseValueSourceUnknown

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

