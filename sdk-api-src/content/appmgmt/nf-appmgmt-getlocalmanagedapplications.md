---
UID: NF:appmgmt.GetLocalManagedApplications
title: GetLocalManagedApplications function (appmgmt.h)
description: The GetLocalManagedApplications function can be run on the target computer to get a list of managed applications on that computer.
helpviewer_keywords: ["GetLocalManagedApplications","GetLocalManagedApplications function [Group Policy]","appmgmt/GetLocalManagedApplications","policy.getlocalmanagedapplications"]
old-location: policy\getlocalmanagedapplications.htm
tech.root: Policy
ms.assetid: 4606ff09-7e23-4953-aeef-cac822995d35
ms.date: 12/05/2018
ms.keywords: GetLocalManagedApplications, GetLocalManagedApplications function [Group Policy], appmgmt/GetLocalManagedApplications, policy.getlocalmanagedapplications
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
 - GetLocalManagedApplications
 - appmgmt/GetLocalManagedApplications
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
 - GetLocalManagedApplications
---

# GetLocalManagedApplications function


## -description

The
    <b>GetLocalManagedApplications</b> function can be run on the target computer to get  a list of managed applications on that computer. The function can also be called in the context of a user to get a list of managed applications for that user. This function only returns applications that can be installed by the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>.

## -parameters

### -param bUserApps [in]

A value that, if <b>TRUE</b>, the <i>prgLocalApps</i> parameter contains a list of managed applications that applies to the user.  If the value of this parameter is <b>FALSE</b>, the <i>prgLocalApps</i> parameter contains a list of managed applications that applies to the local computer.

### -param pdwApps [out]

The address of a <b>DWORD</b> that specifies the number of applications in the list returned by <i>prgLocalApps</i>.

### -param prgLocalApps [out]

The address of an array that contains the list of managed applications. You must call <b>LocalFree</b> to free this array when its contents are no longer required. This parameter cannot be null. The list is returned as a <a href="/windows/desktop/api/appmgmt/ns-appmgmt-localmanagedapplication">LOCALMANAGEDAPPLICATION</a> structure.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-localmanagedapplication">LOCALMANAGEDAPPLICATION</a>