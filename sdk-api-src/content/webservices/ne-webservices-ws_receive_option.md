---
UID: NE:webservices.__unnamed_enum_17
title: WS_RECEIVE_OPTION (webservices.h)
author: windows-sdk-content
description: Specifies whether a message is required when receiving from a channel.
old-location: wsw\ws_receive_option.htm
tech.root: wsw
ms.assetid: a2aefba7-40ff-4399-b13f-f1bad191f366
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_RECEIVE_OPTION, WS_RECEIVE_OPTION enumeration [Web Services for Windows], WS_RECEIVE_OPTIONAL_MESSAGE, WS_RECEIVE_REQUIRED_MESSAGE, webservices/WS_RECEIVE_OPTION, webservices/WS_RECEIVE_OPTIONAL_MESSAGE, webservices/WS_RECEIVE_REQUIRED_MESSAGE, wsw.ws_receive_option
ms.topic: enum
f1_keywords: 
 - "webservices/WS_RECEIVE_OPTION"
dev_langs:
 - c++
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
 - WS_RECEIVE_OPTION
targetos: Windows
req.typenames: WS_RECEIVE_OPTION
req.redist: 
ms.custom: 19H1
---

# WS_RECEIVE_OPTION enumeration


## -description


Specifies whether a message is required when receiving from a channel.
            


## -enum-fields




### -field WS_RECEIVE_REQUIRED_MESSAGE

A message is required to be received.  If the channel does not have
                    any more messages, then the function will fail.
                


### -field WS_RECEIVE_OPTIONAL_MESSAGE

The message is not required to be received.  If the channel does not have any more
                    messages, the function will return <b>WS_S_END</b>.
                (See <a href="https://docs.microsoft.com/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

