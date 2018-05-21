---
UID: NS:webservices._WS_HOST_NAMES
title: "_WS_HOST_NAMES"
author: windows-driver-content
description: A structure containing a list of host names.
old-location: wsw\ws_host_names.htm
old-project: wsw
ms.assetid: 9815eb1e-0ce6-4b56-9f9a-e3938d502b72
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_HOST_NAMES, WS_HOST_NAMES structure [Web Services for Windows], _WS_HOST_NAMES, webservices/WS_HOST_NAMES, wsw.ws_host_names
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
req.typenames: WS_HOST_NAMES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_HOST_NAMES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_HOST_NAMES structure


## -description



                A structure containing a list of host names.
            


## -struct-fields




### -field hostNames


                    A list of host names.  Each host name can be a DNS name or
                    an IPv4 or IPv6 address.  IPv6 addresses are enclosed
                    in brackets ('[' address ']').
                


### -field hostNameCount


                    The number of elements in the hostNames array.
                

