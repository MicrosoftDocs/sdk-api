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

# _INSTALLSPEC structure


## -description


The <b>INSTALLSPEC</b> structure specifies a group policy application by its user-friendly name and group policy GUID or by its file name extension. The <b>Spec</b> member of the <a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>  structure provides this information to the <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> function.


## -struct-fields




### -field AppName

Structure that contains the following members.


### -field AppName.Name

The user-friendly name of the application as it appears in <b>Add or Remove Programs</b> and the <a href="https://msdn.microsoft.com/0fc85897-c96d-457a-a189-6fa0165eb11b">Group Policy Object Editor</a>. You can obtain the name by calling <a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>.


### -field AppName.GPOId

The <b>GUID</b> for the group policy object in which the application exists. You can obtain the group policy object <b>GUID</b> by calling <a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>.


### -field FileExt

The file name extension, such as .jpg,  of the application to be installed.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a> fails if the <b>Type</b> member of <a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a> equals <b>FILEEXT</b> and there is no application deployed to the user with this file name extension.</div>
<div> </div>

### -field ProgId

 


### -field COMClass

 


### -field COMClass.Clsid

 


### -field COMClass.ClsCtx

 




#### - Reserved1

This parameter is reserved and should not be used.


#### - Reserved2

Structure that contains the following members.



#### Reserved1

This parameter is reserved and should not be used.



#### Reserved2

This parameter is reserved and should not be used.


## -see-also




<a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>



<a href="https://msdn.microsoft.com/0c0570c6-f8f5-41e1-a1d2-d4e8c450f73c">INSTALLDATA</a>



<a href="https://msdn.microsoft.com/5b2e1d82-a421-42af-9e1b-391ae9d4813e">InstallApplication</a>



<a href="https://msdn.microsoft.com/d45494e2-d86e-4d94-a158-4024eacf46a2">UninstallApplication</a>
 

 

