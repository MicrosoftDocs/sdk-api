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

# IUpdateInstaller::get_IsBusy


## -description


Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.

This property is read-only.


## -parameters


## -remarks



A new installation or uninstallation is processed only when no other installation or uninstallation is in progress. While an installation or uninstallation is in progress, a new installation or uninstallation immediately fails with the <b>WU_E_OPERATIONINPROGRESS</b> error. The <b>IsBusy</b> property does not secure an opportunity for the caller to begin a new installation or uninstallation. If the <b>IsBusy</b> property or a recent installation or uninstallation failure indicates that another installation or uninstallation is already in progress, the caller should attempt the installation or uninstallation later.




## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

