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

# IGPMConstants::get_SecurityFlags


## -description


Retrieves the value of the 
<b>SecurityFlags</b> property, which represents the portion of the security descriptor to retrieve or set for a GPO. You can pass the returned value in the <i>ulFlags</i> parameter to the 
<a href="https://msdn.microsoft.com/4035119b-2688-4326-8d08-825d53c3d8e2">IGPMGPO::GetSecurityDescriptor</a> and 
<a href="https://msdn.microsoft.com/087cbe19-25d9-4134-8893-1b2906915220">IGPMGPO::SetSecurityDescriptor</a> methods.

This property is read-only.


## -parameters


## -remarks



For more information about access control lists (ACLs) and the security model for controlling access to objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants</a>
 

 

