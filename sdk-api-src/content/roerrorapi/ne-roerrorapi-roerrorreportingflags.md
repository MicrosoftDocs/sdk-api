---
UID: NE:roerrorapi.RoErrorReportingFlags
title: RoErrorReportingFlags
description: Specifies the behavior of the RoOriginateError and RoTransformError functions.
tech.root: winrt
helpviewer_keywords: ["RoErrorReportingFlags"]
ms.assetid: 51C5D2A7-3831-437E-AD7F-AEBC79A7C801
ms.date: 05/20/2019
ms.keywords: RoErrorReportingFlags
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: roerrorapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - roerrorapi/RoErrorReportingFlags
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - roerrorapi.h
api_name:
 - RoErrorReportingFlags
---

# RoErrorReportingFlags


## -description

Specifies the behavior of the [RoOriginateError](nf-roerrorapi-rooriginateerror.md) and [RoTransformError](nf-roerrorapi-rotransformerror.md) functions.

## -enum-fields

### -field None

Error functions raise structured exceptions.

### -field SuppressExceptions

Error functions do not raise structured exceptions, even when a debugger is present.
Override the behavior of this flag by setting the *ForceExceptions* flag.

### -field ForceExceptions

Error functions raise structured exceptions, even if no debugger is present.
This flag supercedes the *SuppressExceptions* flag.
If this flag is set, structured exceptions are raised even if the *SuppressExceptions* flag is set.

### -field UseSetErrorInfo

Error functions report error strings through a COM object that is attached to the COM channel through the **SetErrorInfo** infrastructure.
This flag requires that the calling thread be initialized into COM.

### -field SuppressSetErrorInfo

Error functions do not report error strings through a COM object that is attached to the COM channel through the **SetErrorInfo** infrastructure.

## -remarks

## -see-also

[RoGetErrorReportingFlags](nf-roerrorapi-rogeterrorreportingflags.md)

[RoSetErrorReportingFlags](nf-roerrorapi-roseterrorreportingflags.md)

[RoOriginateError](nf-roerrorapi-rooriginateerror.md)

[RoTransformError](nf-roerrorapi-rotransformerror.md)

