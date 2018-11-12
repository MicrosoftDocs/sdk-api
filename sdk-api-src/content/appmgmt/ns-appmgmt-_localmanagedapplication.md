---
UID: NS:appmgmt._LOCALMANAGEDAPPLICATION
title: "_LOCALMANAGEDAPPLICATION"
author: windows-sdk-content
description: The LOCALMANAGEDAPPLICATION structure describes a managed application installed for a user or a computer. Returned by the GetLocalManagedApplications function.
old-location: policy\localmanagedapplication_str.htm
tech.root: Policy
ms.assetid: b2b7d209-76ee-4ba4-ac61-034d2c8e0689
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PLOCALMANAGEDAPPLICATION, LOCALMANAGEDAPPLICATION, LOCALMANAGEDAPPLICATION structure [Group Policy], LOCAL_STATE_ASSIGNED, LOCAL_STATE_POLICYREMOVE_ORPHAN, LOCAL_STATE_POLICYREMOVE_UNINSTALL, LOCAL_STATE_PUBLISHED, LOCAL_STATE_UNINSTALL_UNMANAGED, PLOCALMANAGEDAPPLICATION, PLOCALMANAGEDAPPLICATION structure pointer [Group Policy], _LOCALMANAGEDAPPLICATION, appmgmt/LOCALMANAGEDAPPLICATION, appmgmt/PLOCALMANAGEDAPPLICATION, policy.localmanagedapplication_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - LOCALMANAGEDAPPLICATION
product: Windows
targetos: Windows
req.typenames: LOCALMANAGEDAPPLICATION, *PLOCALMANAGEDAPPLICATION
req.redist: 
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

This is a Unicode string that gives the <a href="https://msdn.microsoft.com/en-us/library/Cc185688(v=VS.85).aspx">Windows Installer</a> product code GUID for the application.


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
 

 

