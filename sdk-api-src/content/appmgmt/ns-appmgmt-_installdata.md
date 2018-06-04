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

# _INSTALLDATA structure


## -description


The <b>INSTALLDATA</b> structure specifies a group-policy application to  be installed by <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>.


## -struct-fields




### -field Type

Defines  how <b>Spec</b> specifies the application to <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>.     <b>Type</b> can be  one of the <a href="https://msdn.microsoft.com/9e62a22d-cae7-4b3e-9000-71eddb1f3cad">INSTALLSPECTYPE</a> enumeration values. Set <b>Type</b> to APPNAME to install an application specified by its user-friendly name and GPO GUID. Set <b>Type</b> to FILEEXT to install  an application specified by its file name extension.


### -field Spec

An <a href="https://msdn.microsoft.com/e9c1b943-9cb0-480f-8ab7-0f439087216a">INSTALLSPEC</a> structure that specifies the application.


## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/e9c1b943-9cb0-480f-8ab7-0f439087216a">INSTALLSPEC</a>



<a href="https://msdn.microsoft.com/9e62a22d-cae7-4b3e-9000-71eddb1f3cad">INSTALLSPECTYPE</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/d45494e2-d86e-4d94-a158-4024eacf46a2">UninstallApplication</a>
 

 

