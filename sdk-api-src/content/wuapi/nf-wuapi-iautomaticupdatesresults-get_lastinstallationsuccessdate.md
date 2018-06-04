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

# IAutomaticUpdatesResults::get_LastInstallationSuccessDate


## -description


Gets the last time and Coordinated Universal Time (UTC) date when Automatic Updates successfully installed any updates, even if some failures occurred.

This property is read-only.


## -parameters


## -remarks



Calls to <b>LastInstallationSuccessDate</b> by public users do not update this property. Only the <a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">AutomaticUpdates</a> object will update this property.




## -see-also




<a href="https://msdn.microsoft.com/fe9a5ea3-9d59-450b-8c5e-3444ec13dc97">IAutomaticUpdatesResults</a>
 

 

