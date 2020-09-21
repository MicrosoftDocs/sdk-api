---
UID: NF:appmgmt.GetManagedApplications
title: GetManagedApplications function (appmgmt.h)
description: The GetManagedApplications function gets a list of applications that are displayed in the Add pane of Add/Remove Programs (ARP) for a specified user context.
helpviewer_keywords: ["GetManagedApplications","GetManagedApplications function [Group Policy]","MANAGED_APPS_FROMCATEGORY","MANAGED_APPS_USERAPPLICATIONS","appmgmt/GetManagedApplications","policy.getmanagedapplications"]
old-location: policy\getmanagedapplications.htm
tech.root: Policy
ms.assetid: 62e32f36-cbb2-4557-9773-8bd454870d55
ms.date: 12/05/2018
ms.keywords: GetManagedApplications, GetManagedApplications function [Group Policy], MANAGED_APPS_FROMCATEGORY, MANAGED_APPS_USERAPPLICATIONS, appmgmt/GetManagedApplications, policy.getmanagedapplications
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetManagedApplications
 - appmgmt/GetManagedApplications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - GetManagedApplications
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

This parameter is a pointer to an array of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-managedapplication">MANAGEDAPPLICATION</a> structures. This array contains the list of applications listed in the <b>Add</b> pane of  <b>Add/Remove Programs</b> (ARP). You must call <b>LocalFree</b> to free the array when they array is no longer required.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>