---
UID: NS:webservices._WS_FAULT_REASON
title: WS_FAULT_REASON (webservices.h)
description: Contains an explanation of the fault.
helpviewer_keywords: ["WS_FAULT_REASON","WS_FAULT_REASON structure [Web Services for Windows]","webservices/WS_FAULT_REASON","wsw.ws_fault_reason"]
old-location: wsw\ws_fault_reason.htm
tech.root: wsw
ms.assetid: 70ec3d18-00ab-4dde-8a8a-b200eda44acd
ms.date: 12/05/2018
ms.keywords: WS_FAULT_REASON, WS_FAULT_REASON structure [Web Services for Windows], webservices/WS_FAULT_REASON, wsw.ws_fault_reason
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
req.typenames: WS_FAULT_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_FAULT_REASON
 - webservices/_WS_FAULT_REASON
 - WS_FAULT_REASON
 - webservices/WS_FAULT_REASON
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
 - WS_FAULT_REASON
---

# WS_FAULT_REASON structure


## -description

Contains an explanation of the fault.

## -struct-fields

### -field text

Text describing the fault.

### -field lang

The language identifier that identifies the language of the text.
                

The identifier is serialized using the xml:lang attribute, and has
                    values that follow <a href="https://www.ietf.org/rfc/rfc3066.txt">RFC3066.txt</a>.

