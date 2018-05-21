---
UID: NS:webservices._WS_XML_SECURITY_TOKEN_PROPERTY
title: "_WS_XML_SECURITY_TOKEN_PROPERTY"
author: windows-driver-content
description: Specifies a property for an XML security token.
old-location: wsw\ws_xml_security_token_property.htm
old-project: wsw
ms.assetid: dd235e33-39f7-459d-8b7f-76d5c3f96770
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_XML_SECURITY_TOKEN_PROPERTY, WS_XML_SECURITY_TOKEN_PROPERTY structure [Web Services for Windows], _WS_XML_SECURITY_TOKEN_PROPERTY, webservices/WS_XML_SECURITY_TOKEN_PROPERTY, wsw.ws_xml_security_token_property
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
req.typenames: WS_XML_SECURITY_TOKEN_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_SECURITY_TOKEN_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_SECURITY_TOKEN_PROPERTY structure


## -description



                Specifies a property for an XML security token.
            


## -struct-fields




### -field id


                Identifies the <a href="https://msdn.microsoft.com/78133ccf-4e3c-4c1b-97af-1a487b444ee0">WS_XML_SECURITY_TOKEN_PROPERTY_ID</a>.
            


### -field value


                A pointer to the value.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize


                The size in bytes of the memory pointed to by value.
            

