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

# tagUpdateServiceOption enumeration


## -description


Defines the options that  affect how the service registration for a scan package service is removed.


## -enum-fields




### -field usoNonVolatileService

Indicates that you must call the <a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">IUpdateServiceManager::RemoveService</a> method to remove the service registration. 

Failure to call the <a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">RemoveService</a> method before releasing the <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface causes a resource leak.


## -remarks



If you do not specify <b>usoNonVolatileService</b>, the service registration is automatically removed when you release the <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface.

The <b>UpdateServiceOption</b> enumeration  may require that you update Windows Update Agent (WUA). For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b0677bb-9f19-4bb4-9942-8ca3da18b29a">IUpdateServiceManager::AddScanPackageService</a>
 

 

