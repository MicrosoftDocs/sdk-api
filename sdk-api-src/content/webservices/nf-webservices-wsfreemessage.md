---
UID: NF:webservices.WsFreeMessage
title: WsFreeMessage function (webservices.h)
description: Releases the memory resource associated with a Message object.
old-location: wsw\wsfreemessage.htm
tech.root: wsw
ms.assetid: 50e08300-9445-4741-9298-bd80fc777041
ms.date: 12/05/2018
ms.keywords: WsFreeMessage, WsFreeMessage function [Web Services for Windows], webservices/WsFreeMessage, wsw.wsfreemessage
f1_keywords:
- webservices/WsFreeMessage
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WebServices.dll
api_name:
- WsFreeMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsFreeMessage function


## -description


Releases the memory resource associated with a Message object.
            


## -parameters




### -param message [in]

A pointer to the <b>Message</b> object to release.  The pointer must reference a valid <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object returned
                    by <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscreatemessage">WsCreateMessage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscreatemessageforchannel">WsCreateMessageForChannel</a> and the referenced value may not be <b>NULL</b>.
                
                


## -returns



This function does not return a value.



