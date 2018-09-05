---
UID: NS:webservices._WS_XML_BUFFER_PROPERTY
title: "_WS_XML_BUFFER_PROPERTY"
author: windows-sdk-content
description: Specifies an XML buffer&#8211;specific setting.
old-location: wsw\ws_xml_buffer_property.htm
old-project: wsw
ms.assetid: bec8d297-7f5a-4b8f-a333-9b535358c470
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_XML_BUFFER_PROPERTY, WS_XML_BUFFER_PROPERTY structure [Web Services for Windows], _WS_XML_BUFFER_PROPERTY, webservices/WS_XML_BUFFER_PROPERTY, wsw.ws_xml_buffer_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.redist: 
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
req.typenames: WS_XML_BUFFER_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_BUFFER_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_BUFFER_PROPERTY structure


## -description


Specifies an XML buffer–specific setting.
      


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/580a72d3-6800-48b3-9345-4e3b20bb4066">WS_XML_BUFFER_PROPERTY_ID</a>.
        


### -field value

A pointer to the value to set.
            The pointer must have an alignment compatible with the type
            of the property.
        


### -field valueSize

The size in bytes of the memory pointed to by value.
        

