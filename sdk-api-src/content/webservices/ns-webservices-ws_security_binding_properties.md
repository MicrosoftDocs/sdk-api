---
UID: NS:webservices._WS_SECURITY_BINDING_PROPERTIES
title: WS_SECURITY_BINDING_PROPERTIES (webservices.h)
description: Specifies an array of security binding settings.
helpviewer_keywords: ["WS_SECURITY_BINDING_PROPERTIES","WS_SECURITY_BINDING_PROPERTIES structure [Web Services for Windows]","webservices/WS_SECURITY_BINDING_PROPERTIES","wsw.ws_security_binding_properties"]
old-location: wsw\ws_security_binding_properties.htm
tech.root: wsw
ms.assetid: 4b36e801-dea9-44fe-ae12-104ea7dce1ee
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_BINDING_PROPERTIES, WS_SECURITY_BINDING_PROPERTIES structure [Web Services for Windows], webservices/WS_SECURITY_BINDING_PROPERTIES, wsw.ws_security_binding_properties
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
targetos: Windows
req.typenames: WS_SECURITY_BINDING_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_BINDING_PROPERTIES
 - webservices/_WS_SECURITY_BINDING_PROPERTIES
 - WS_SECURITY_BINDING_PROPERTIES
 - webservices/WS_SECURITY_BINDING_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_BINDING_PROPERTIES
---

# WS_SECURITY_BINDING_PROPERTIES structure


## -description

Specifies an array of security binding settings.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
          using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
          is 0.

### -field propertyCount

The number of elements in the properties array.

