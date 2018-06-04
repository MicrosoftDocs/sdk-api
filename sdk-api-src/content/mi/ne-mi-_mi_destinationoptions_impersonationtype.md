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

# _MI_DestinationOptions_ImpersonationType enumeration


## -description


Used by the DCOM protocol handler to specify how impersonation is done on the server.


## -enum-fields




### -field MI_DestinationOptions_ImpersonationType_Default

Use the default impersonation.


### -field MI_DestinationOptions_ImpersonationType_None

Do not impersonate.


### -field MI_DestinationOptions_ImpersonationType_Identify

Identify user only.


### -field MI_DestinationOptions_ImpersonationType_Impersonate

Allow impersonation of user.


### -field MI_DestinationOptions_ImpersonationType_Delegate

This option relates to Kerberos delegation and needs to be enabled on the domain.

