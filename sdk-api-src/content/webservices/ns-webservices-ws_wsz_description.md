---
UID: NS:webservices._WS_WSZ_DESCRIPTION
title: WS_WSZ_DESCRIPTION (webservices.h)
description: This type description is used with WS_WSZ_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized.
helpviewer_keywords: ["WS_WSZ_DESCRIPTION","WS_WSZ_DESCRIPTION structure [Web Services for Windows]","webservices/WS_WSZ_DESCRIPTION","wsw.ws_wsz_description"]
old-location: wsw\ws_wsz_description.htm
tech.root: wsw
ms.assetid: 12b6f630-7585-4c88-8c49-f37d1899d32b
ms.date: 12/05/2018
ms.keywords: WS_WSZ_DESCRIPTION, WS_WSZ_DESCRIPTION structure [Web Services for Windows], webservices/WS_WSZ_DESCRIPTION, wsw.ws_wsz_description
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
req.typenames: WS_WSZ_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_WSZ_DESCRIPTION
 - webservices/_WS_WSZ_DESCRIPTION
 - WS_WSZ_DESCRIPTION
 - webservices/WS_WSZ_DESCRIPTION
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
 - WS_WSZ_DESCRIPTION
---

# WS_WSZ_DESCRIPTION structure


## -description

This type description is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a> and is optional.
                It is used to specify constraints on the set of values
                which can be deserialized.

## -struct-fields

### -field minCharCount

Specifies the minimum number of characters (not including the terminating '\0' character).

### -field maxCharCount

Specifies the maximum number of characters (not including the terminating '\0' character).