---
UID: NS:webservices._WS_ATTRIBUTE_DESCRIPTION
title: WS_ATTRIBUTE_DESCRIPTION (webservices.h)
author: windows-sdk-content
description: Represents a mapping between a C data type and an XML attribute.
old-location: wsw\ws_attribute_description.htm
tech.root: wsw
ms.assetid: 23a97842-2d9f-438a-89a7-2dd0e381a019
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_ATTRIBUTE_DESCRIPTION, WS_ATTRIBUTE_DESCRIPTION structure [Web Services for Windows], webservices/WS_ATTRIBUTE_DESCRIPTION, wsw.ws_attribute_description
ms.topic: struct
f1_keywords: 
 - "webservices/WS_ATTRIBUTE_DESCRIPTION"
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WS_ATTRIBUTE_DESCRIPTION
targetos: Windows
req.typenames: WS_ATTRIBUTE_DESCRIPTION
req.redist: 
ms.custom: 19H1
---

# WS_ATTRIBUTE_DESCRIPTION structure


## -description


Represents a mapping between a C data type and an XML attribute.


## -struct-fields




### -field attributeLocalName

The local name of the XML attribute.


### -field attributeNs

The namespace of the XML attribute.


### -field type

The type that corresponds to the XML attribute.
                

Not all types support being read and written as attributes.  If the
                    documentation for the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> indicates it supports
                    <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_ATTRIBUTE_TYPE_MAPPING</a>, then it can be used with this structure.
                


### -field typeDescription

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.
                

