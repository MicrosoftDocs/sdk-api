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

# tagServerSelection enumeration


## -description


Defines the update services that Windows Update can operate against. 


## -enum-fields




### -field ssDefault

Used only by <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>. Indicates that the search call should search the default server.

The default server used by the Windows Update Agent (WUA) is the same as <b>ssMangagedServer</b> if the computer is set up to have a managed server. If the computer is not been set up to have a managed server, WUA uses the first update service for which the <a href="https://msdn.microsoft.com/17b51a04-69f6-4a96-880b-ef57f75253ae">IsRegisteredWithAU</a> property of <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> is VARIANT_TRUE and the <a href="https://msdn.microsoft.com/1a473cb3-7209-4056-91bc-bfa416981ae5">IsManaged</a> property of <b>IUpdateService</b> is VARIANT_FALSE


### -field ssManagedServer

Indicates the managed server, in an environment that uses Windows Server Update Services or a similar corporate update server to manage the computer.


### -field ssWindowsUpdate

Indicates the Windows Update service.


### -field ssOthers

Indicates some update service other than those listed previously. If the <b>ServerSelection</b> property of a Windows Update Agent API object is set to <b>ssOthers</b>, then the <b>ServiceID</b> property of the object contains the ID of the service.

