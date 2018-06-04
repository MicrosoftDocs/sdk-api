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

# FAX_SMTP_AUTHENTICATION_TYPE_ENUM enumeration


## -description


The <b>FAX_SMTP_AUTHENTICATION_TYPE_ENUM</b> enumeration defines the configuration options for delivery receipts sent through email.


## -enum-fields




### -field fsatANONYMOUS

The server sends fax transmission receipts using a nonauthenticated SMTP protocol. 


### -field fsatBASIC

The server sends fax transmission receipts using a basic (plain text) authenticated SMTP protocol. 


### -field fsatNTLM

The server sends fax transmission receipts using an NTLM-authenticated SMTP protocol. 


## -see-also




<a href="https://msdn.microsoft.com/1624ad8c-07ca-4ab1-970c-fb0624903b81">IFaxReceiptOptions::get_AuthenticationType</a>
 

 

