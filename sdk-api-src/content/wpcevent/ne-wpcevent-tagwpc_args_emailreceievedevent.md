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

# tagWPC_ARGS_EMAILRECEIEVEDEVENT enumeration


## -description


Indicates information about an email message that has been received.


## -enum-fields




### -field WPC_ARGS_EMAILRECEIEVEDEVENT_SENDER

The sender who sent the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_APPNAME

The name of the application that sent the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_APPVERSION

The version of the application that sent the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_SUBJECT

The subject line of the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_REASON

The reason given for the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_RECIPCOUNT

The number of accounts that received the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_RECIPIENT

The recipient account that received the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_ATTACHCOUNT

The number of attachments in the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_ATTACHMENTNAME

The name of the attachment in the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_RECEIVEDTIME

The time that the email message was received.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_EMAILACCOUNT

The email account that sent the email message.


### -field WPC_ARGS_EMAILRECEIEVEDEVENT_CARGS

The arguments for the email message.

