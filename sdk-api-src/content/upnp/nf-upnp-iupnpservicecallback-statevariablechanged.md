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

# IUPnPServiceCallback::StateVariableChanged


## -description


The 
<b>StateVariableChanged</b> method is invoked when a state variable has changed.


## -parameters




### -param pus [in]

Reference to an 
<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> object that specifies the service about which the UPnP framework is sending the notification.


### -param pcwszStateVarName [in]

Reference to a string that specifies the name of the state variable that has changed.


### -param vaValue






#### - varValue [in]

Specifies the new value. The type of the data returned depends on the data type of the state variable for which the notification is sent.


## -returns



The application should return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>



<a href="https://msdn.microsoft.com/f5797907-ae65-48e6-adf8-b717bfb5101f">IUPnPService::AddCallback</a>



<a href="https://msdn.microsoft.com/44515be4-891b-4f3d-a2c2-1699e468e708">IUPnPServiceCallback</a>
 

 

