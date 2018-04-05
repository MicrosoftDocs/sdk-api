---
UID: NS:webservices._WS_SECURITY_PROPERTY
title: "_WS_SECURITY_PROPERTY"
author: windows-driver-content
description: Specifies a channel-wide security setting.
old-location: wsw\ws_security_property.htm
old-project: wsw
ms.assetid: 676079cd-6ca8-486b-9604-172423210ad5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_SECURITY_PROPERTY, WS_SECURITY_PROPERTY structure [Web Services for Windows], _WS_SECURITY_PROPERTY, webservices/WS_SECURITY_PROPERTY, wsw.ws_security_property
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
req.typenames: WS_SECURITY_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_PROPERTY structure


## -description



                Specifies a channel-wide security setting.
            


## -struct-fields




### -field id


                Identifies the <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ID</a>.
            


### -field value


                A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.
            


### -field valueSize


                The size in bytes of the memory pointed to by value.
            

