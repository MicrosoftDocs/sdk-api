---
UID: NS:appmgmt._LOCALMANAGEDAPPLICATION
title: LOCALMANAGEDAPPLICATION (appmgmt.h)
description: The LOCALMANAGEDAPPLICATION structure describes a managed application installed for a user or a computer. Returned by the GetLocalManagedApplications function.
helpviewer_keywords: ["*PLOCALMANAGEDAPPLICATION","LOCALMANAGEDAPPLICATION","LOCALMANAGEDAPPLICATION structure [Group Policy]","LOCAL_STATE_ASSIGNED","LOCAL_STATE_POLICYREMOVE_ORPHAN","LOCAL_STATE_POLICYREMOVE_UNINSTALL","LOCAL_STATE_PUBLISHED","LOCAL_STATE_UNINSTALL_UNMANAGED","PLOCALMANAGEDAPPLICATION","PLOCALMANAGEDAPPLICATION structure pointer [Group Policy]","appmgmt/LOCALMANAGEDAPPLICATION","appmgmt/PLOCALMANAGEDAPPLICATION","policy.localmanagedapplication_str"]
old-location: policy\localmanagedapplication_str.htm
tech.root: Policy
ms.assetid: b2b7d209-76ee-4ba4-ac61-034d2c8e0689
ms.date: 12/05/2018
ms.keywords: '*PLOCALMANAGEDAPPLICATION, LOCALMANAGEDAPPLICATION, LOCALMANAGEDAPPLICATION structure [Group Policy], LOCAL_STATE_ASSIGNED, LOCAL_STATE_POLICYREMOVE_ORPHAN, LOCAL_STATE_POLICYREMOVE_UNINSTALL, LOCAL_STATE_PUBLISHED, LOCAL_STATE_UNINSTALL_UNMANAGED, PLOCALMANAGEDAPPLICATION, PLOCALMANAGEDAPPLICATION structure pointer [Group Policy], appmgmt/LOCALMANAGEDAPPLICATION, appmgmt/PLOCALMANAGEDAPPLICATION, policy.localmanagedapplication_str'
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
targetos: Windows
req.typenames: LOCALMANAGEDAPPLICATION, *PLOCALMANAGEDAPPLICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALMANAGEDAPPLICATION
 - appmgmt/_LOCALMANAGEDAPPLICATION
 - PLOCALMANAGEDAPPLICATION
 - appmgmt/PLOCALMANAGEDAPPLICATION
 - LOCALMANAGEDAPPLICATION
 - appmgmt/LOCALMANAGEDAPPLICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - LOCALMANAGEDAPPLICATION
---

# LOCALMANAGEDAPPLICATION structure


## -description

The <b>LOCALMANAGEDAPPLICATION</b> structure describes a managed application installed for a user or a computer. Returned by the <a href="/windows/desktop/api/appmgmt/nf-appmgmt-getlocalmanagedapplications">GetLocalManagedApplications</a> function.

## -struct-fields

### -field pszDeploymentName

This is a Unicode string that gives the user friendly name of the application as it appears in the Application Deployment Editor (ADE).

### -field pszPolicyName

This is the user-friendly name of the group policy object (GPO) from which the application originates.

### -field pszProductId

This is a Unicode string that gives the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> product code GUID for the application.

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

<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>