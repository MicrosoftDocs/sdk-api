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

# UalRegisterProduct function


## -description


Registers a product with User Access Logging (UAL).


## -parameters




### -param wszProductName [in]

The name of the major product to register with UAL. For example, "Windows Server".


### -param wszRoleName [in]

The name of the role or minor product within the major product to be registered with UAL. For example, "DHCP".


### -param wszGuid

TBD




#### - wszRoleGuid [in]

The GUID associated with the role specified by the <i>wszRoleName</i> parameter.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.



