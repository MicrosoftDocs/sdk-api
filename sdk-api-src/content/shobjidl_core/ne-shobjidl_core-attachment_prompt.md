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

# ATTACHMENT_PROMPT enumeration


## -description


Provides a set of flags to be used with <a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">IAttachmentExecute::Prompt</a> to indicate the type of prompt UI to display.


## -enum-fields




### -field ATTACHMENT_PROMPT_NONE

Do not use.


### -field ATTACHMENT_PROMPT_SAVE

Displays a prompt asking whether the user would like to save the attachment.


### -field ATTACHMENT_PROMPT_EXEC

Displays a prompt asking whether the user would like to execute the attachment.


### -field ATTACHMENT_PROMPT_EXEC_OR_SAVE

Displays a prompt giving the user a choice of executing or saving the attachment.

