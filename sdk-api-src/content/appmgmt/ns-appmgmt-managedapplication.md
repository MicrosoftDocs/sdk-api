---
UID: NS:appmgmt._MANAGEDAPPLICATION
title: MANAGEDAPPLICATION (appmgmt.h)
description: The MANAGEDAPPLICATION structure contains information about an application. The function GetManagedApplications returns an array of MANAGEDAPPLICATION structures.
helpviewer_keywords: ["*PMANAGEDAPPLICATION","MANAGEDAPPLICATION","MANAGEDAPPLICATION structure [Group Policy]","MANAGED_APPTYPE_SETUPEXE","MANAGED_APPTYPE_UNSUPPORTED","MANAGED_APPTYPE_WINDOWSINSTALLER","PMANAGEDAPPLICATION","PMANAGEDAPPLICATION structure pointer [Group Policy]","appmgmt/MANAGEDAPPLICATION","appmgmt/PMANAGEDAPPLICATION","policy.managedapplication_str"]
old-location: policy\managedapplication_str.htm
tech.root: Policy
ms.assetid: 8ac78f92-e665-4dd0-b226-6bf41dcd050a
ms.date: 12/05/2018
ms.keywords: '*PMANAGEDAPPLICATION, MANAGEDAPPLICATION, MANAGEDAPPLICATION structure [Group Policy], MANAGED_APPTYPE_SETUPEXE, MANAGED_APPTYPE_UNSUPPORTED, MANAGED_APPTYPE_WINDOWSINSTALLER, PMANAGEDAPPLICATION, PMANAGEDAPPLICATION structure pointer [Group Policy], appmgmt/MANAGEDAPPLICATION, appmgmt/PMANAGEDAPPLICATION, policy.managedapplication_str'
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
req.typenames: MANAGEDAPPLICATION, *PMANAGEDAPPLICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MANAGEDAPPLICATION
 - appmgmt/_MANAGEDAPPLICATION
 - PMANAGEDAPPLICATION
 - appmgmt/PMANAGEDAPPLICATION
 - MANAGEDAPPLICATION
 - appmgmt/MANAGEDAPPLICATION
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
 - MANAGEDAPPLICATION
---

# MANAGEDAPPLICATION structure


## -description

The <b>MANAGEDAPPLICATION</b> structure contains information about an application. The function <a href="/windows/desktop/api/appmgmt/nf-appmgmt-getmanagedapplications">GetManagedApplications</a> returns an array of <b>MANAGEDAPPLICATION</b> structures.

## -struct-fields

### -field pszPackageName

The user-friendly name of the application.

### -field pszPublisher

The name of the application's publisher.

### -field dwVersionHi

The major version number of the application.

### -field dwVersionLo

The minor version number of the application.

### -field dwRevision

The version number of the deployment. The version changes each time an application gets patched.

### -field GpoId

The GUID of the GPO from which this application is deployed.

### -field pszPolicyName

The user-friendly name for the GPO from which this application is deployed.

### -field ProductId

If this application is installed by <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>, this member is the ProductId GUID.

### -field Language

The numeric language identifier that indicates the language version of the application. For a list of language numeric identifiers, see the <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a> topic.

### -field pszOwner

This member is unused.

### -field pszCompany

This member is unused.

### -field pszComments

This member is unused.

### -field pszContact

This member is unused.

### -field pszSupportUrl

This member is unused.

### -field dwPathType

Indicates the type of package used to install the application. This member can have one of the following values.



#### MANAGED_APPTYPE_WINDOWSINSTALLER

The application is installed using the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>.



#### MANAGED_APPTYPE_SETUPEXE

The application is installed using a legacy setup application.



#### MANAGED_APPTYPE_UNSUPPORTED

The application is installed by an unsupported setup application.

### -field bInstalled

This parameter is <b>TRUE</b> if the application is currently installed and  is <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/appmgmt/nf-appmgmt-getmanagedapplications">GetManagedApplications</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>