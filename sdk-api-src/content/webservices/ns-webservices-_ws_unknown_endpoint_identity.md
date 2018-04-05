---
UID: NS:webservices._WS_UNKNOWN_ENDPOINT_IDENTITY
title: "_WS_UNKNOWN_ENDPOINT_IDENTITY"
author: windows-driver-content
description: Type for unknown endpoint identity. This type is only used to represent an endpoint identity type that was deserialized but was not understood.
old-location: wsw\ws_unknown_endpoint_identity.htm
old-project: wsw
ms.assetid: 93a51fe5-7195-4286-97f3-92c20b0d3e54
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_UNKNOWN_ENDPOINT_IDENTITY, WS_UNKNOWN_ENDPOINT_IDENTITY structure [Web Services for Windows], _WS_UNKNOWN_ENDPOINT_IDENTITY, webservices/WS_UNKNOWN_ENDPOINT_IDENTITY, wsw.ws_unknown_endpoint_identity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WS_UNKNOWN_ENDPOINT_IDENTITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_UNKNOWN_ENDPOINT_IDENTITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_UNKNOWN_ENDPOINT_IDENTITY structure


## -description



                Type for unknown endpoint identity.  This type is only used to represent
                an endpoint identity type that was deserialized but was not understood.
            


## -struct-fields




### -field identity


                    The base type from which this type and all other endpoint identity types derive.
                


### -field element


                    An XML buffer containing a single XML Element which corresponds to the
                    identity element that was not understood.  This field may not be <b>NULL</b>.
                

