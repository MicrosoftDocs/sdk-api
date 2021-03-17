---
UID: NS:webservices._WS_SECURITY_PROPERTIES
title: WS_SECURITY_PROPERTIES (webservices.h)
description: Specifies an array of channel-wide security settings.
helpviewer_keywords: ["WS_SECURITY_PROPERTIES","WS_SECURITY_PROPERTIES structure [Web Services for Windows]","webservices/WS_SECURITY_PROPERTIES","wsw.ws_security_properties"]
old-location: wsw\ws_security_properties.htm
tech.root: wsw
ms.assetid: 36a2dca5-d49f-4af7-ac1a-0ff7e9331e9a
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_PROPERTIES, WS_SECURITY_PROPERTIES structure [Web Services for Windows], webservices/WS_SECURITY_PROPERTIES, wsw.ws_security_properties
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
req.typenames: WS_SECURITY_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_PROPERTIES
 - webservices/_WS_SECURITY_PROPERTIES
 - WS_SECURITY_PROPERTIES
 - webservices/WS_SECURITY_PROPERTIES
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
 - WS_SECURITY_PROPERTIES
---

# WS_SECURITY_PROPERTIES structure


## -description

Specifies an array of channel-wide security settings.

## -struct-fields

### -field properties

An array of properties.  The number of elements in the array is specified
          using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
          is 0.

### -field propertyCount

The number of elements in the properties array.

