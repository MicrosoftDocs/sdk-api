---
UID: NE:webservices.__unnamed_enum_10
title: "__unnamed_enum_10"
author: windows-sdk-content
description: A set of flags used within a WS_FIELD_DESCRIPTION.
old-location: wsw\ws_field_options.htm
tech.root: wsw
ms.assetid: 85271aa4-665e-413a-be42-da6f91706bf0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_FIELD_NILLABLE, WS_FIELD_NILLABLE_ITEM, WS_FIELD_OPTIONAL, WS_FIELD_OPTIONS, WS_FIELD_OPTIONS enumeration [Web Services for Windows], WS_FIELD_OTHER_NAMESPACE, WS_FIELD_POINTER, __unnamed_enum_10, webservices/WS_FIELD_NILLABLE, webservices/WS_FIELD_NILLABLE_ITEM, webservices/WS_FIELD_OPTIONAL, webservices/WS_FIELD_OPTIONS, webservices/WS_FIELD_OTHER_NAMESPACE, webservices/WS_FIELD_POINTER, wsw.ws_field_options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_FIELD_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_10 enumeration


## -description


A set of flags used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
            


## -enum-fields




### -field WS_FIELD_POINTER

For some <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s there is an option to either embed the type in the parent structure
                    or to point to it. For those types, the default is to embed. When this flag is specified,
                    the type is assumed to be a pointer instead.  Types that are always pointers (like <b>WS_WSZ_TYPE</b>and <b>WS_XML_BUFFER_TYPE</b>) do not have this flag set.  See the documentation for a 
                    specific <b>WS_TYPE</b> to see if the type supports this flag.
                

This flag may only be used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>,
                    <b>WS_REPEATING_ELEMENT_FIELD_MAPPING</b>, <b>WS_ANY_ELEMENT_FIELD_MAPPING</b>or <b>WS_NO_FIELD_MAPPING</b>.
                


### -field WS_FIELD_OPTIONAL

The meaning of this flag is defined by the <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> used
                    for the field.
                


### -field WS_FIELD_NILLABLE

This flag may only be used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>or <b>WS_REPEATING_ELEMENT_FIELD_MAPPING</b>.
                

When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>, this flag indicates
                    that the element may contain an xsi:nil attribute used to
                    indicate a value which is nil. See the documentation for an individual 
                    <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> to determine whether a nil value is supported for that type, 
                    and how nil is represented for that type.
                

When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, this flag indicates
                    that the array wrapper element may contain an xsi:nil attribute used to
                    indicate a value which is nil.  In this case, a nil array is distinguished from
                    a zero size array based on whether or not the array pointer is <b>NULL</b> (in either
                    case the count is zero).
                


### -field WS_FIELD_NILLABLE_ITEM

This flag may only be used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>.
                

This indicates that the repeating values may contain an xsi:nil attribute
                    which indicates a nil value.
                    See the documentation for an individual <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> to determine
                    whether a nil value is supported for that type, and how a nil value is represented
                    for that type.
                

To control whether or not the array itself is nillable, see <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>.
                


### -field WS_FIELD_OTHER_NAMESPACE

This flag may only be used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>.
                

This indicates that only elements that do not match the namespace specified
                    in the ns field of the <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a> are allowed.  This
                    is similar to the schema construct "##other".
                


## -remarks



For more information on which flag combinations are valid for which types, 
                see the documentation for each individual <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>.
            



