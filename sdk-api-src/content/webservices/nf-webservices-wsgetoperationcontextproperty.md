---
UID: NF:webservices.WsGetOperationContextProperty
title: WsGetOperationContextProperty function (webservices.h)
description: Returns a property of the specified operation context. It should be noted that the validity of these property is limited to the lifetime of the operation context itself.
helpviewer_keywords: ["WsGetOperationContextProperty","WsGetOperationContextProperty function [Web Services for Windows]","webservices/WsGetOperationContextProperty","wsw.wsgetoperationcontextproperty"]
old-location: wsw\wsgetoperationcontextproperty.htm
tech.root: wsw
ms.assetid: 9ab843ff-8f2c-424e-8bb9-ba71f9355728
ms.date: 12/05/2018
ms.keywords: WsGetOperationContextProperty, WsGetOperationContextProperty function [Web Services for Windows], webservices/WsGetOperationContextProperty, wsw.wsgetoperationcontextproperty
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsGetOperationContextProperty
 - webservices/WsGetOperationContextProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetOperationContextProperty
---

# WsGetOperationContextProperty function


## -description

Returns a property of the specified operation context. It should be noted that the 
                validity of these property is limited to the lifetime of the operation context itself.

## -parameters

### -param context [in]

The context that the property value is being obtained for.

### -param id [in]

The id of the property.

### -param value

The address to place the retrieved value. The contents are not modified in case of a failure.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The size of the buffer that the caller has allocated for the retrieved value.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

