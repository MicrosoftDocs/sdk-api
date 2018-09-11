---
UID: NF:webservices.WsFreeMessage
title: WsFreeMessage function
author: windows-sdk-content
description: Releases the memory resource associated with a Message object.
old-location: wsw\wsfreemessage.htm
tech.root: wsw
ms.assetid: 50e08300-9445-4741-9298-bd80fc777041
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsFreeMessage, WsFreeMessage function [Web Services for Windows], webservices/WsFreeMessage, wsw.wsfreemessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsFreeMessage function


## -description


Releases the memory resource associated with a Message object.
            


## -parameters




### -param message [in]

A pointer to the <b>Message</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> object returned
                    by <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> or <a href="https://msdn.microsoft.com/0a4f076b-6725-45a9-8817-5dec3b647c4f">WsCreateMessageForChannel</a> and the referenced value may not be <b>NULL</b>.
                
                


## -returns



This function does not return a value.



