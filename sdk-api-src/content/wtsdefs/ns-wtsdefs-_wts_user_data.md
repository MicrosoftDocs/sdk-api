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

# _WTS_USER_DATA structure


## -description


Contains select client property values.


## -struct-fields




### -field WorkDirectory

A string value that specifies the directory where the client startup program resides. This value corresponds to the <b>WorkDirectory</b> member of the <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WTS_CLIENT_DATA</a> structure.


### -field InitialProgram

A string value that specifies the name of  the initial program. This value corresponds to the <b>InitialProgram</b> member of the <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WTS_CLIENT_DATA</a> structure.


### -field UserTimeZone

A <a href="https://msdn.microsoft.com/7d0e75b1-0a9b-47b1-8bf7-192966e3d19a">WTS_TIME_ZONE_INFORMATION</a> structure that contains client time zone information. This value corresponds to the <b>ClientTimeZone</b> member of the <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WTS_CLIENT_DATA</a> structure.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/fa77c537-c78d-4fe3-b597-787efd740cf6">GetUserData</a> method and is both sent to and returned by the protocol. This structure is initialized with client data by the Remote Desktop Services service. If a value does not exist for a member, the protocol should not provide one.



