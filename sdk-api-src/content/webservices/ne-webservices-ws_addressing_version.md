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

# WS_ADDRESSING_VERSION enumeration


## -description


Identifies the version of the specification used for
                the addressing headers.
            


## -enum-fields




### -field WS_ADDRESSING_VERSION_0_9


                    The message addressing headers correspond to version 0.9 (August 2004)
                    of the addressing specification <a href=" http://go.microsoft.com/fwlink/p/?linkid=139712">Web Services Addressing (WS-Addressing)</a>.
                


### -field WS_ADDRESSING_VERSION_1_0


                    The message addressing headers correspond to version 1.0 (May 2006)
                    of the addressing specification <a href=" http://go.microsoft.com/fwlink/p/?linkid=139713">Web Services Addressing 1.0 - Core</a>.
                


### -field WS_ADDRESSING_VERSION_TRANSPORT


                    This addressing version indicates that the only addressing headers
                    supported are those that are natively supported by the underlying
                    transport (there are no addressing-related headers that are transmitted
                    as part of the SOAP envelope).
                


                    The <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_ACTION_HEADER</a> and <b>WS_TO_HEADER</b> are
                    automatically mapped to/from the transport-specific message locations
                    when messages are sent/received.  Use of other <b>WS_HEADER_TYPE</b>
                    are not supported for this addressing version.
                


                    This addressing version is only supported for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
                    Since the SOAP over HTTP protocol does not support sending an action on a reply,
                    the value of the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_ACTION_HEADER</a> will not be transmitted by the channel.
                

