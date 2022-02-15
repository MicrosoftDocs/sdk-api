---
UID: NE:webservices.__unnamed_enum_31
title: WS_EXCEPTION_CODE (webservices.h)
description: The structured exception codes thrown by this component. These exceptions are fatal and should not be handled by the application.
helpviewer_keywords: ["WS_EXCEPTION_CODE","WS_EXCEPTION_CODE enumeration [Web Services for Windows]","WS_EXCEPTION_CODE_INTERNAL_FAILURE","WS_EXCEPTION_CODE_USAGE_FAILURE","webservices/WS_EXCEPTION_CODE","webservices/WS_EXCEPTION_CODE_INTERNAL_FAILURE","webservices/WS_EXCEPTION_CODE_USAGE_FAILURE","wsw.ws_exception_code"]
old-location: wsw\ws_exception_code.htm
tech.root: wsw
ms.assetid: b59cbd41-03f2-4938-842a-664eddb07b1b
ms.date: 12/05/2018
ms.keywords: WS_EXCEPTION_CODE, WS_EXCEPTION_CODE enumeration [Web Services for Windows], WS_EXCEPTION_CODE_INTERNAL_FAILURE, WS_EXCEPTION_CODE_USAGE_FAILURE, webservices/WS_EXCEPTION_CODE, webservices/WS_EXCEPTION_CODE_INTERNAL_FAILURE, webservices/WS_EXCEPTION_CODE_USAGE_FAILURE, wsw.ws_exception_code
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
req.typenames: WS_EXCEPTION_CODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_EXCEPTION_CODE
 - webservices/WS_EXCEPTION_CODE
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
 - WS_EXCEPTION_CODE
---

# WS_EXCEPTION_CODE enumeration


## -description

The structured exception codes thrown by this component.  These
                exceptions are fatal and should not be handled by the application.

## -enum-fields

### -field WS_EXCEPTION_CODE_USAGE_FAILURE:0xC03D0000

This exception occurs to indicate that usage of the web services component 
                    has violated the API contract.

### -field WS_EXCEPTION_CODE_INTERNAL_FAILURE:0xc03d0001

This exception occurs to indicate that an internal error occurred in the 
                    web services component.

