---
UID: NS:webservices._WS_ANY_ATTRIBUTE
title: WS_ANY_ATTRIBUTE (webservices.h)
description: This type is used to store an attribute that has not been directly mapped to a field.
helpviewer_keywords: ["WS_ANY_ATTRIBUTE","WS_ANY_ATTRIBUTE structure [Web Services for Windows]","webservices/WS_ANY_ATTRIBUTE","wsw.ws_any_attribute"]
old-location: wsw\ws_any_attribute.htm
tech.root: wsw
ms.assetid: 31900554-24d9-44f5-a774-7d3245f5e646
ms.date: 12/05/2018
ms.keywords: WS_ANY_ATTRIBUTE, WS_ANY_ATTRIBUTE structure [Web Services for Windows], webservices/WS_ANY_ATTRIBUTE, wsw.ws_any_attribute
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
req.typenames: WS_ANY_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ANY_ATTRIBUTE
 - webservices/_WS_ANY_ATTRIBUTE
 - WS_ANY_ATTRIBUTE
 - webservices/WS_ANY_ATTRIBUTE
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
 - WS_ANY_ATTRIBUTE
---

# WS_ANY_ATTRIBUTE structure


## -description

This type is used to store an attribute
                that has not been directly mapped to a field.

## -struct-fields

### -field localName

Specifies the localName of the attribute.

### -field ns

Specifies the namespace of the attribute.

### -field value

Specifies the value of the attribute.  This
                    field may not be <b>NULL</b>.

## -remarks

This structure is used with <a href="/windows/desktop/api/webservices/ns-webservices-ws_any_attributes">WS_ANY_ATTRIBUTES</a>.