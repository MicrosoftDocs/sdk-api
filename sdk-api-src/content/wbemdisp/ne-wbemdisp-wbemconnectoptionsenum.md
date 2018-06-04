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

# WbemConnectOptionsEnum enumeration


## -description


The 
WbemConnectOptionsEnum constant defines a security flag that is used as a parameter in calls to 
the <a href="https://msdn.microsoft.com/31364c68-b031-4cf0-851f-b4e302f077e0">SWbemLocator.ConnectServer</a> method when a connection to WMI on a remote machine is failing.


## -enum-fields




### -field wbemConnectFlagUseMaxWait

Shortens the timeout for the <a href="https://msdn.microsoft.com/31364c68-b031-4cf0-851f-b4e302f077e0">SWbemLocator.ConnectServer</a> method call to two minutes.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

