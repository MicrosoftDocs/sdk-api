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

# IUpdate::get_LastDeploymentChangeTime


## -description


Gets the last published date of the update,  in Coordinated Universal Time (UTC) date and time,  on the server that deploys the update.

This property is read-only.


## -parameters


## -remarks



On computers that are running Windows XP, the <b>LastDeploymentChangeTime</b> property retrieves the same date and time that are retrieved by the  <a href="http://go.microsoft.com/fwlink/p/?linkid=121339">CreationDate</a> property  of the <b>IUpdateApproval</b> interface. The <a href="http://go.microsoft.com/fwlink/p/?linkid=121339">CreationDate</a> property is used on computers that are running Windows Server 2003.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

