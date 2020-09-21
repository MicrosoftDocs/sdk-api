---
UID: NS:webservices._WS_PARAMETER_DESCRIPTION
title: WS_PARAMETER_DESCRIPTION (webservices.h)
description: The index of the parameters in the incoming/outgoing messages field descriptions.
helpviewer_keywords: ["WS_PARAMETER_DESCRIPTION","WS_PARAMETER_DESCRIPTION structure [Web Services for Windows]","webservices/WS_PARAMETER_DESCRIPTION","wsw.ws_parameter_description"]
old-location: wsw\ws_parameter_description.htm
tech.root: wsw
ms.assetid: 357ac313-7ad2-411f-802e-d08ecf648710
ms.date: 12/05/2018
ms.keywords: WS_PARAMETER_DESCRIPTION, WS_PARAMETER_DESCRIPTION structure [Web Services for Windows], webservices/WS_PARAMETER_DESCRIPTION, wsw.ws_parameter_description
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
targetos: Windows
req.typenames: WS_PARAMETER_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_PARAMETER_DESCRIPTION
 - webservices/_WS_PARAMETER_DESCRIPTION
 - WS_PARAMETER_DESCRIPTION
 - webservices/WS_PARAMETER_DESCRIPTION
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
 - WS_PARAMETER_DESCRIPTION
---

# WS_PARAMETER_DESCRIPTION structure


## -description

The index of the parameters in the incoming/outgoing messages field descriptions.

## -struct-fields

### -field parameterType

The type of the parameter.

### -field inputMessageIndex

A value between 0 and MAX_SHORT - 1 that represents the index of the field 
                    in the input <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a>. It is MAX_USHORT if it has not present in the input
                    WS_MESSAGE.

### -field outputMessageIndex

A value between 0 and MAX_SHORT - 1 that represents the index of the field 
                    in the output <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a>. It is MAX_USHORT if it has not present in the output
                    WS_MESSAGE.