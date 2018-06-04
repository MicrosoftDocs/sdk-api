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

# UIAutomationType enumeration


## -description


Contains values used to indicate Microsoft UI Automation data types.


## -enum-fields




### -field UIAutomationType_Int

An integer.


### -field UIAutomationType_Bool

An Boolean value.


### -field UIAutomationType_String

A null-terminated character string.


### -field UIAutomationType_Double

A double-precision floating-point number.


### -field UIAutomationType_Point

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the x- and y-coordinates of a point.


### -field UIAutomationType_Rect

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the coordinates of the upper-left and lower-right corners of a rectangle. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_Element

The address of the <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interface of a UI Automation element.


### -field UIAutomationType_Array

An array of an unspecified type.


### -field UIAutomationType_Out

The address of a variable that receives a value retrieved by a function.


### -field UIAutomationType_IntArray

An array of integers. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_BoolArray

An array of Boolean values. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_StringArray

An array of null-terminated character strings. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_DoubleArray

An array of double-precision floating-point numbers. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_PointArray

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures, each containing the x- and y-coordinates of a point. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_RectArray

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures, each containing the coordinates of the upper-left and lower-right corners of a rectangle. This type is not supported for a custom UI Automation property.


### -field UIAutomationType_ElementArray

An array of pointers to <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interfaces, each for a UI Automation element.


### -field UIAutomationType_OutInt

The address of a variable that receives an integer value.


### -field UIAutomationType_OutBool

The address of a variable that receives a Boolean value.


### -field UIAutomationType_OutString

The address of a variable that receives a null-terminated character string.


### -field UIAutomationType_OutDouble

The address of a variable that receives a double-precision floating-point number.


### -field UIAutomationType_OutPoint

The address of a variable that receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure.


### -field UIAutomationType_OutRect

The address of a variable that receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure.


### -field UIAutomationType_OutElement

The address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interface of a UI Automation element.


### -field UIAutomationType_OutIntArray

The address of a variable that receives an array of integer values.


### -field UIAutomationType_OutBoolArray

The address of a variable that receives an array of Boolean values.


### -field UIAutomationType_OutStringArray

The address of a variable that receives an array of null-terminated character strings.


### -field UIAutomationType_OutDoubleArray

The address of a variable that receives an array of double-precision floating-point numbers.


### -field UIAutomationType_OutPointArray

The address of a variable that receives an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures.


### -field UIAutomationType_OutRectArray

The address of a variable that receives an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures.


### -field UIAutomationType_OutElementArray

The address of a variable that receives an array of pointers to the <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interfaces of UI Automation elements.

