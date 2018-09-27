---
UID: NF:appmgmt.GetManagedApplications
title: GetManagedApplications function
author: windows-sdk-content
description: The GetManagedApplications function gets a list of applications that are displayed in the Add pane of Add/Remove Programs (ARP) for a specified user context.
old-location: policy\getmanagedapplications.htm
tech.root: Policy
ms.assetid: 62e32f36-cbb2-4557-9773-8bd454870d55
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetManagedApplications, GetManagedApplications function [Group Policy], MANAGED_APPS_FROMCATEGORY, MANAGED_APPS_USERAPPLICATIONS, appmgmt/GetManagedApplications, policy.getmanagedapplications
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - GetManagedApplications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetManagedApplications function


## -description


The
    <b>GetManagedApplications</b> function gets a list of applications that are displayed in the <b>Add</b> pane of <b>Add/Remove Programs</b> (ARP) for a specified user context.


## -parameters




### -param pCategory [in]

A pointer to a GUID that specifies the  category  

of applications to be listed. If <i>pCategory</i> is not null, <i>dwQueryFlags</i> must   contain <b>MANAGED_APPS_FROMCATEGORY</b>. If <i>pCategory</i> is null, <i>dwQueryFlags</i> cannot contain <b>MANAGED_APPS_FROMCATEGORY</b>.


### -param dwQueryFlags [in]

This parameter can contain one or more of the following values.



#### MANAGED_APPS_USERAPPLICATIONS

Lists all applications that apply to the user. The parameter <i>pCategory</i> must be null.



#### MANAGED_APPS_FROMCATEGORY

Lists only applications in the category specified by <i>pCategory</i>.   The <i>pCategory</i> parameter cannot be null.


### -param dwInfoLevel [in]

This parameter must be <b>MANAGED_APPS_INFOLEVEL_DEFAULT</b>.


### -param pdwApps [out]

The count of applications in the list returned by this function.


### -param prgManagedApps [out]

This parameter is a pointer to an array of <a href="https://msdn.microsoft.com/8ac78f92-e665-4dd0-b226-6bf41dcd050a">MANAGEDAPPLICATION</a> structures. This array contains the list of applications listed in the <b>Add</b> pane of  <b>Add/Remove Programs</b> (ARP). You must call <b>LocalFree</b> to free the array when they array is no longer required.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

