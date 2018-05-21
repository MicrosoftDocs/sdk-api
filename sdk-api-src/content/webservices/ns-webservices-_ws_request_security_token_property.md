---
UID: NS:webservices._WS_REQUEST_SECURITY_TOKEN_PROPERTY
title: "_WS_REQUEST_SECURITY_TOKEN_PROPERTY"
author: windows-driver-content
description: Specifies a property for requesting a security token from an issuer.
old-location: wsw\ws_request_security_token_property.htm
old-project: wsw
ms.assetid: ebf6d821-f540-4c89-a2f8-c795a3688e0d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_PROPERTY, WS_REQUEST_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows], _WS_REQUEST_SECURITY_TOKEN_PROPERTY, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY, wsw.ws_request_security_token_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_REQUEST_SECURITY_TOKEN_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_REQUEST_SECURITY_TOKEN_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_REQUEST_SECURITY_TOKEN_PROPERTY structure


## -description



                Specifies a property for requesting a security token from an issuer.
            


## -struct-fields




### -field id


                Identifies the <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID</a>.
            


### -field value


                A pointer to the value.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize


                The size in bytes of the memory pointed to by value.
            

