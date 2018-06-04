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

# _LOCALMANAGEDAPPLICATION structure


## -description


The <b>LOCALMANAGEDAPPLICATION</b> structure describes a managed application installed for a user or a computer. Returned by the <a href="https://msdn.microsoft.com/4606ff09-7e23-4953-aeef-cac822995d35">GetLocalManagedApplications</a> function.


## -struct-fields




### -field pszDeploymentName

This is a Unicode string that gives the user friendly name of the application as it appears in the Application Deployment Editor (ADE).


### -field pszPolicyName

This is the user-friendly name of the group policy object (GPO) from which the application originates.


### -field pszProductId

This is a Unicode string that gives the <a href="setup.windows_installer_start_page">Windows Installer</a> product code GUID for the application.


### -field dwState

Indicates the  state of the installed application. This parameter can contain one or more of the following values.



#### LOCAL_STATE_ASSIGNED

The application is installed in the assigned state.



#### LOCAL_STATE_PUBLISHED

The application is installed in the published state.



#### LOCAL_STATE_UNINSTALL_UNMANAGED

The installation of this application uninstalled an unmanaged application with a conflicting transform.



#### LOCAL_STATE_POLICYREMOVE_ORPHAN

If the policy from which this application originates is removed, the application is  left on the computer.



#### LOCAL_STATE_POLICYREMOVE_UNINSTALL

If the policy from which this application originates is removed, the application is uninstalled from the computer.


## -see-also




<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>
 

 

