---
UID: NS:appmgmt._MANAGEDAPPLICATION
title: "_MANAGEDAPPLICATION"
author: windows-sdk-content
description: The MANAGEDAPPLICATION structure contains information about an application. The function GetManagedApplications returns an array of MANAGEDAPPLICATION structures.
old-location: policy\managedapplication_str.htm
tech.root: Policy
ms.assetid: 8ac78f92-e665-4dd0-b226-6bf41dcd050a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PMANAGEDAPPLICATION, MANAGEDAPPLICATION, MANAGEDAPPLICATION structure [Group Policy], MANAGED_APPTYPE_SETUPEXE, MANAGED_APPTYPE_UNSUPPORTED, MANAGED_APPTYPE_WINDOWSINSTALLER, PMANAGEDAPPLICATION, PMANAGEDAPPLICATION structure pointer [Group Policy], _MANAGEDAPPLICATION, appmgmt/MANAGEDAPPLICATION, appmgmt/PMANAGEDAPPLICATION, policy.managedapplication_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MANAGEDAPPLICATION
product: Windows
targetos: Windows
req.typenames: MANAGEDAPPLICATION, *PMANAGEDAPPLICATION
req.redist: 
---

# _MANAGEDAPPLICATION structure


## -description


The <b>MANAGEDAPPLICATION</b> structure contains information about an application. The function <a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a> returns an array of <b>MANAGEDAPPLICATION</b> structures.


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

If this application is installed by <a href="setup.windows_installer_start_page">Windows Installer</a>, this member is the ProductId GUID.


### -field Language

The numeric language identifier that indicates the language version of the application. For a list of language numeric identifiers, see the <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a> topic.


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

The application is installed using the <a href="setup.windows_installer_start_page">Windows Installer</a>.



#### MANAGED_APPTYPE_SETUPEXE

The application is installed using a legacy setup application.



#### MANAGED_APPTYPE_UNSUPPORTED

The application is installed by an unsupported setup application.


### -field bInstalled

This parameter is <b>TRUE</b> if the application is currently installed and  is <b>FALSE</b> otherwise.


## -see-also




<a href="https://msdn.microsoft.com/62e32f36-cbb2-4557-9773-8bd454870d55">GetManagedApplications</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>
 

 

