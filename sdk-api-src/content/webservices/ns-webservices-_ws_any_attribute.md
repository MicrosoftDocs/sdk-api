---
UID: NS:webservices._WS_ANY_ATTRIBUTE
title: "_WS_ANY_ATTRIBUTE"
author: windows-driver-content
description: This type is used to store an attribute that has not been directly mapped to a field.
old-location: wsw\ws_any_attribute.htm
old-project: wsw
ms.assetid: 31900554-24d9-44f5-a774-7d3245f5e646
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_ANY_ATTRIBUTE, WS_ANY_ATTRIBUTE structure [Web Services for Windows], _WS_ANY_ATTRIBUTE, webservices/WS_ANY_ATTRIBUTE, wsw.ws_any_attribute
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
req.typenames: WS_ANY_ATTRIBUTE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_ANY_ATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ANY_ATTRIBUTE structure


## -description



                This type is used to store an attribute
                that has not been directly mapped to a field.
            


## -struct-fields




### -field localName


                    Specifies the localName of the attribute.
                


### -field ns


                    Specifies the namespace of the attribute.
                


### -field value


                    Specifies the value of the attribute.  This
                    field may not be <b>NULL</b>.
                


## -remarks




                This structure is used with <a href="https://msdn.microsoft.com/6c428c99-755f-40ab-bc9e-e1a7a3d70c1d">WS_ANY_ATTRIBUTES</a>.
            



