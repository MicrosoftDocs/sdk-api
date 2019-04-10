---
UID: NE:webservices.__unnamed_enum_68
title: WS_EXTENDED_PROTECTION_SCENARIO (webservices.h)
author: windows-sdk-content
description: Defines how Extended Protection is validated.
old-location: wsw\ws_extended_protection_scenario.htm
tech.root: wsw
ms.assetid: bd4a41aa-10bc-445c-9664-49f284881bf8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_EXTENDED_PROTECTION_SCENARIO, WS_EXTENDED_PROTECTION_SCENARIO enumeration [Web Services for Windows], WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER, WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL, webservices/WS_EXTENDED_PROTECTION_SCENARIO, webservices/WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER, webservices/WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL, wsw.ws_extended_protection_scenario
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_EXTENDED_PROTECTION_SCENARIO
product: Windows
targetos: Windows
req.typenames: WS_EXTENDED_PROTECTION_SCENARIO
req.redist: 
---

# WS_EXTENDED_PROTECTION_SCENARIO enumeration


## -description


Defines how <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a> is validated. For most configurations, the runtime can automatically determine what needs to 
                be validated based on the presence of the <a href="https://msdn.microsoft.com/en-us/library/Dd323441(v=VS.85).aspx">WS_SSL_TRANSPORT_SECURITY_BINDING</a>. However, if the SSL connection is terminated at 
                an intermediary such as a proxy prior to reaching the server then the validation method must change, and this scenario cannot be automatically detected.
            

Only available on the server.
            


## -enum-fields




### -field WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER

There is no SSL connection between the client and the server, or the SSL connection is terminated at the server. This is the default.
                


### -field WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL

An SSL connection exists but is terminated at an intermediary. The connection between the intermediary and the server may or may not
                    use SSL. When this property is set, <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ID</a> must be set as well.
                

