---
UID: NE:webservices.WS_ADDRESSING_VERSION
title: WS_ADDRESSING_VERSION
author: windows-sdk-content
description: Identifies the version of the specification used for the addressing headers.
old-location: wsw\ws_addressing_version.htm
tech.root: wsw
ms.assetid: 87f60067-109c-456c-b060-33ab840872e0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_ADDRESSING_VERSION, WS_ADDRESSING_VERSION enumeration [Web Services for Windows], WS_ADDRESSING_VERSION_0_9, WS_ADDRESSING_VERSION_1_0, WS_ADDRESSING_VERSION_TRANSPORT, webservices/WS_ADDRESSING_VERSION, webservices/WS_ADDRESSING_VERSION_0_9, webservices/WS_ADDRESSING_VERSION_1_0, webservices/WS_ADDRESSING_VERSION_TRANSPORT, wsw.ws_addressing_version
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - WS_ADDRESSING_VERSION
product: Windows
targetos: Windows
req.typenames: WS_ADDRESSING_VERSION
req.redist: 
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
                    when messages are sent/received.  Use of other <b>WS_HEADER_TYPE</b>are not supported for this addressing version.
                

This addressing version is only supported for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
                    Since the SOAP over HTTP protocol does not support sending an action on a reply,
                    the value of the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_ACTION_HEADER</a> will not be transmitted by the channel.
                

