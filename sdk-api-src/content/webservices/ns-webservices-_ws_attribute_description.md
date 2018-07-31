---
UID: NS:webservices._WS_ATTRIBUTE_DESCRIPTION
title: "_WS_ATTRIBUTE_DESCRIPTION"
author: windows-sdk-content
description: Represents a mapping between a C data type and an XML attribute.
old-location: wsw\ws_attribute_description.htm
old-project: wsw
ms.assetid: 23a97842-2d9f-438a-89a7-2dd0e381a019
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_ATTRIBUTE_DESCRIPTION, WS_ATTRIBUTE_DESCRIPTION structure [Web Services for Windows], _WS_ATTRIBUTE_DESCRIPTION, webservices/WS_ATTRIBUTE_DESCRIPTION, wsw.ws_attribute_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_ATTRIBUTE_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ATTRIBUTE_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ATTRIBUTE_DESCRIPTION structure


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
                    documentation for the <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> indicates it supports
                    <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>, then it can be used with this structure.
                


### -field typeDescription

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>.
                

