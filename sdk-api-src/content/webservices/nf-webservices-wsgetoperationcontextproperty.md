---
UID: NF:webservices.WsGetOperationContextProperty
title: WsGetOperationContextProperty function
author: windows-sdk-content
description: Returns a property of the specified operation context. It should be noted that the validity of these property is limited to the lifetime of the operation context itself.
old-location: wsw\wsgetoperationcontextproperty.htm
tech.root: wsw
ms.assetid: 9ab843ff-8f2c-424e-8bb9-ba71f9355728
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsGetOperationContextProperty, WsGetOperationContextProperty function [Web Services for Windows], webservices/WsGetOperationContextProperty, wsw.wsgetoperationcontextproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetOperationContextProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



