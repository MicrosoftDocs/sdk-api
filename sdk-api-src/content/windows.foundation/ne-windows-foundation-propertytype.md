---
UID: NE:windows.foundation.PropertyType
title: PropertyType (windows.foundation.h)
author: windows-sdk-content
description: Identifies the type that is stored in a Windows Runtime object that implements the IPropertyValue interface.
old-location: winrt\propertytype.htm
tech.root: WinRT
ms.assetid: A4DC4348-88EE-48FB-91ED-F1D12FC89EE1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropertyType, PropertyType enumeration [Windows Runtime], PropertyType_Boolean, PropertyType_BooleanArray, PropertyType_Char16, PropertyType_Char16Array, PropertyType_DateTime, PropertyType_DateTimeArray, PropertyType_Double, PropertyType_DoubleArray, PropertyType_Empty, PropertyType_Guid, PropertyType_GuidArray, PropertyType_Inspectable, PropertyType_InspectableArray, PropertyType_Int16, PropertyType_Int16Array, PropertyType_Int32, PropertyType_Int32Array, PropertyType_Int64, PropertyType_Int64Array, PropertyType_OtherType, PropertyType_OtherTypeArray, PropertyType_Point, PropertyType_PointArray, PropertyType_Rect, PropertyType_RectArray, PropertyType_Single, PropertyType_SingleArray, PropertyType_Size, PropertyType_SizeArray, PropertyType_String, PropertyType_StringArray, PropertyType_TimeSpan, PropertyType_TimeSpanArray, PropertyType_UInt16, PropertyType_UInt16Array, PropertyType_UInt32, PropertyType_UInt32Array, PropertyType_UInt64, PropertyType_UInt64Array, PropertyType_UInt8, PropertyType_UInt8Array, windows/PropertyType, windows/PropertyType_Boolean, windows/PropertyType_BooleanArray, windows/PropertyType_Char16, windows/PropertyType_Char16Array, windows/PropertyType_DateTime, windows/PropertyType_DateTimeArray, windows/PropertyType_Double, windows/PropertyType_DoubleArray, windows/PropertyType_Empty, windows/PropertyType_Guid, windows/PropertyType_GuidArray, windows/PropertyType_Inspectable, windows/PropertyType_InspectableArray, windows/PropertyType_Int16, windows/PropertyType_Int16Array, windows/PropertyType_Int32, windows/PropertyType_Int32Array, windows/PropertyType_Int64, windows/PropertyType_Int64Array, windows/PropertyType_OtherType, windows/PropertyType_OtherTypeArray, windows/PropertyType_Point, windows/PropertyType_PointArray, windows/PropertyType_Rect, windows/PropertyType_RectArray, windows/PropertyType_Single, windows/PropertyType_SingleArray, windows/PropertyType_Size, windows/PropertyType_SizeArray, windows/PropertyType_String, windows/PropertyType_StringArray, windows/PropertyType_TimeSpan, windows/PropertyType_TimeSpanArray, windows/PropertyType_UInt16, windows/PropertyType_UInt16Array, windows/PropertyType_UInt32, windows/PropertyType_UInt32Array, windows/PropertyType_UInt64, windows/PropertyType_UInt64Array, windows/PropertyType_UInt8, windows/PropertyType_UInt8Array, winrt.propertytype
ms.topic: enum
f1_keywords: ["windows.foundation/PropertyType"]
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windows.Foundation.h
api_name:
 - PropertyType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropertyType enumeration


## -description


Identifies the type that is stored in a Windows Runtime object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface.


## -enum-fields




### -field PropertyType_Empty

The object does not contain a value.


### -field PropertyType_UInt8

The object contains an unsigned 8-bit integer.


### -field PropertyType_Int16

The object contains a signed 16-bit integer.


### -field PropertyType_UInt16

The object contains an unsigned 16-bit integer.


### -field PropertyType_Int32

The object contains a signed 32-bit integer.


### -field PropertyType_UInt32

The object contains an unsigned 32-bit integer.


### -field PropertyType_Int64

The object contains a signed 64-bit integer.


### -field PropertyType_UInt64

The object contains an unsigned 64-bit integer.


### -field PropertyType_Single

The object contains a 32-bit floating point value. This value conforms to the IEEE 754 standard.


### -field PropertyType_Double

The object contains a 64-bit floating point value. This value conforms to the IEEE 754 standard.


### -field PropertyType_Char16

The object contains a 16-bit character. This character represents a UTF-16 (Unicode) code unit.


### -field PropertyType_Boolean

The object contains an 8-bit Boolean value.


### -field PropertyType_String

The object contains an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>.


### -field PropertyType_Inspectable

The object contains an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface.


### -field PropertyType_DateTime

The object contains a <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a>.


### -field PropertyType_TimeSpan

The object contains a <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a>.


### -field PropertyType_Guid

The object contains a GUID.


### -field PropertyType_Point

The object contains a <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a>.


### -field PropertyType_Size

The object contains a <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a>.


### -field PropertyType_Rect

The object contains a <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a>.


### -field PropertyType_OtherType

The object contains an unspecified type.


### -field PropertyType_UInt8Array

The object contains an array of unsigned 8-bit integers.


### -field PropertyType_Int16Array

The object contains an array of signed 16-bit integers.


### -field PropertyType_UInt16Array

The object contains an array of unsigned 16-bit integers.


### -field PropertyType_Int32Array

The object contains an array of signed 32-bit integers.


### -field PropertyType_UInt32Array

The object contains an array of unsigned 32-bit integers.


### -field PropertyType_Int64Array

The object contains an array of signed 64-bit integers.


### -field PropertyType_UInt64Array

The object contains an array of unsigned 64-bit integers.


### -field PropertyType_SingleArray

The object contains an array of 32-bit floating point values.


### -field PropertyType_DoubleArray

The object contains an array of 64-bit floating point values.


### -field PropertyType_Char16Array

The object contains an array of 16-bit characters.


### -field PropertyType_BooleanArray

The object contains an array of 8-bit Boolean values.


### -field PropertyType_StringArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>.


### -field PropertyType_InspectableArray

The object contains an array of objects that implement the <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface.


### -field PropertyType_DateTimeArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a>.


### -field PropertyType_TimeSpanArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a>.


### -field PropertyType_GuidArray

The object contains an array of GUIDs.


### -field PropertyType_PointArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a>.


### -field PropertyType_SizeArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a>.


### -field PropertyType_RectArray

The object contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a>.


### -field PropertyType_OtherTypeArray

The object contains an array of an unspecified type.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
 

 

