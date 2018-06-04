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

# DDiscMaster2Events::NotifyDeviceAdded


## -description


Receives notification when an optical media device is added to the computer. 


## -parameters




### -param object [in]

An <a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a> interface that you can use to enumerate the devices on the computer. 

This parameter is a <b>MsftDiscMaster2</b> object in script.


### -param uniqueId [in]

String that contains an identifier that uniquely identifies the optical media device that was added to the computer.


## -returns



Return values are ignored.




## -see-also




<a href="https://msdn.microsoft.com/f01fa2d8-989d-499f-b79d-495108640aa2">DDiscMaster2Events</a>



<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>
 

 

