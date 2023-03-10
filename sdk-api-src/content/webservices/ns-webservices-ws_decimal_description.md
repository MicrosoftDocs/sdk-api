---
UID: NS:webservices._WS_DECIMAL_DESCRIPTION
title: WS_DECIMAL_DESCRIPTION (webservices.h)
description: An optional type description used with WS_DECIMAL_TYPE. It is used to specify constraints on the set of values which can be deserialized.
helpviewer_keywords: ["WS_DECIMAL_DESCRIPTION","WS_DECIMAL_DESCRIPTION structure [Web Services for Windows]","webservices/WS_DECIMAL_DESCRIPTION","wsw.ws_decimal_description"]
old-location: wsw\ws_decimal_description.htm
tech.root: wsw
ms.assetid: c2e8fc81-1a09-456c-b8bb-9160bc286ec2
ms.date: 12/05/2018
ms.keywords: WS_DECIMAL_DESCRIPTION, WS_DECIMAL_DESCRIPTION structure [Web Services for Windows], webservices/WS_DECIMAL_DESCRIPTION, wsw.ws_decimal_description
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
req.typenames: WS_DECIMAL_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DECIMAL_DESCRIPTION
 - webservices/_WS_DECIMAL_DESCRIPTION
 - WS_DECIMAL_DESCRIPTION
 - webservices/WS_DECIMAL_DESCRIPTION
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
 - WS_DECIMAL_DESCRIPTION
---

# WS_DECIMAL_DESCRIPTION structure


## -description

An optional type description used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_DECIMAL_TYPE</a>.
                It is used to specify constraints on the set of values
                which can be deserialized.

## -struct-fields

### -field minValue

The minimum value.

### -field maxValue

The maximum value.