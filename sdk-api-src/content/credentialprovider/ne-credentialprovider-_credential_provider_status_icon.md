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

# _CREDENTIAL_PROVIDER_STATUS_ICON enumeration


## -description


Indicates which status icon should be displayed.


## -enum-fields




### -field CPSI_NONE

No icon indicated.


### -field CPSI_ERROR

Display the error icon.


### -field CPSI_WARNING

Display the warning icon.


### -field CPSI_SUCCESS

Reserved.


## -remarks



<b>CREDENTIAL_PROVIDER_STATUS_ICON</b> is not used starting in Windows 10.

As part of <a href="https://msdn.microsoft.com/13d6dda7-4a4f-45bf-af91-72f80497b9f7">ReportResult</a>, a credential provider may specify a status icon to display. It is important to not that only Logon UI calls <b>ReportResult</b>, Credential UI does not.



