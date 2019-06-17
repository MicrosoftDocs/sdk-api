---
UID: NS:webservices._WS_MESSAGE_DESCRIPTION
title: WS_MESSAGE_DESCRIPTION (webservices.h)
author: windows-sdk-content
description: The schema for the input/output WS_MESSAGE for a given operation description.
old-location: wsw\ws_message_description.htm
tech.root: wsw
ms.assetid: 399b3363-004b-499a-9726-0b2513826f43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_MESSAGE_DESCRIPTION, WS_MESSAGE_DESCRIPTION structure [Web Services for Windows], webservices/WS_MESSAGE_DESCRIPTION, wsw.ws_message_description
ms.topic: struct
f1_keywords: ["webservices/WS_MESSAGE_DESCRIPTION"]
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
 - WS_MESSAGE_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_MESSAGE_DESCRIPTION
req.redist: 
ms.custom: 19H1
---

# WS_MESSAGE_DESCRIPTION structure


## -description


The schema for the input/output <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-message">WS_MESSAGE</a> for a given operation description. 
            


## -struct-fields




### -field action

The action associated with the respective input/output <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-message">WS_MESSAGE</a>.
                

If the message does not have an action, this field can be <b>NULL</b>.
                


### -field bodyElementDescription

The description of the value within the body of the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-message">WS_MESSAGE</a>.
                

If <b>NULL</b>, then the message body is assumed to be empty.
                

If non-<b>NULL</b>, this value is read or written as described in
                    <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wswritebody">WsWriteBody</a> and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadbody">WsReadBody</a>.
                

