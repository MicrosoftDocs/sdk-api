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

# IPackageExecutionStateChangeNotification::OnStateChanged


## -description


Called when package state changes during Windows Store app debugging.


## -parameters




### -param pszPackageFullName [in]

The package full name.


### -param pesNewState [in]

The new state that the package changed to.


## -returns



Return <b>S_OK</b> when you implement the <b>OnStateChanged</b>
		 method. 




## -see-also




<a href="https://msdn.microsoft.com/6AD9A9CD-933B-432F-A124-48092588C5DF">IPackageExecutionStateChangeNotification</a>



<a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>
 

 

