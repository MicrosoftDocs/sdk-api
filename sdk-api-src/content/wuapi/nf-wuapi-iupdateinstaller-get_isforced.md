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

# IUpdateInstaller::get_IsForced


## -description


Gets or sets a Boolean value that indicates whether  to  forcibly install or uninstall an update.

This property is read/write.


## -parameters


## -remarks



A forced installation is an installation in which an update is installed even if the metadata indicates that the update is already installed.  A forced uninstallation is an uninstallation in which an update is removed even if the metadata indicates that the update is not installed.

Before you use <b>IsForced</b> to force an installation, determine whether the update is installed and available. If an update is not  installed, a forced installation fails. For example, an update can be downloaded, and then its corresponding files removed from the cache after the expiration limit.   In this case, if the files are not installed, a forced installation of the update  fails.




## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

