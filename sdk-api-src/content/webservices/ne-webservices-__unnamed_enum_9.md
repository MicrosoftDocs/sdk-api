---
UID: NE:webservices.__unnamed_enum_9
title: "__unnamed_enum_9"
author: windows-sdk-content
description: A set of flags used within a WS_STRUCT_DESCRIPTION.
old-location: wsw\ws_struct_options.htm
tech.root: wsw
ms.assetid: 0730f29d-15c5-467b-bb7e-32fde044802d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_STRUCT_ABSTRACT, WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT, WS_STRUCT_IGNORE_UNHANDLED_ATTRIBUTES, WS_STRUCT_OPTIONS, WS_STRUCT_OPTIONS enumeration [Web Services for Windows], __unnamed_enum_9, webservices/WS_STRUCT_ABSTRACT, webservices/WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT, webservices/WS_STRUCT_IGNORE_UNHANDLED_ATTRIBUTES, webservices/WS_STRUCT_OPTIONS, wsw.ws_struct_options
ms.prod: windows
ms.technology: windows-sdk
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
 - WS_STRUCT_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_9 enumeration


## -description


A set of flags used within a <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a>.


## -enum-fields




### -field WS_STRUCT_ABSTRACT

Indicates the type is an abstract type that cannot be serialized
                    or deserialized.  Abstract types are used as base types
                    for other types and are not created directly.
                

This value may only be specified if the <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a>contains a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a> that specifies
                    <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TYPE_ATTRIBUTE_FIELD_MAPPING</a>.
                


### -field WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT

Indicates trailing element content of the structure before the end of the structure element should
                    be ignored and discarded during deserialization. The flag is ignored unless it is used with
                    <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>.
                

This flag can be used for extensibility such that current structure can interoperate with future version
                    where new fields might be added at the end of the structure.
                


### -field WS_STRUCT_IGNORE_UNHANDLED_ATTRIBUTES

Indicates unhandled attributes of the element should be ignored and discarded during
                    deserialization. The flag is ignored unless it is used with
                    <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>.
                

his flag can be used for extensibility such that current structure can interoperate with future version
                    where new attributes might be added.
                

