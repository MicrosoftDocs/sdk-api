---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# WS_EXTENDED_PROTECTION_SCENARIO enumeration


## -description



                Defines how <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a> is validated. For most configurations, the runtime can automatically determine what needs to 
                be validated based on the presence of the <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>. However, if the SSL connection is terminated at 
                an intermediary such as a proxy prior to reaching the server then the validation method must change, and this scenario cannot be automatically detected.
            


                Only available on the server.
            


## -enum-fields




### -field WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER


                    There is no SSL connection between the client and the server, or the SSL connection is terminated at the server. This is the default.
                


### -field WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL


                    An SSL connection exists but is terminated at an intermediary. The connection between the intermediary and the server may or may not
                    use SSL. When this property is set, <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ID</a> must be set as well.
                

