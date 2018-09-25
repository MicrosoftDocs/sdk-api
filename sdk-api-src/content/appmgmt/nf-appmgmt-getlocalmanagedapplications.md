---
UID: NF:appmgmt.GetLocalManagedApplications
title: GetLocalManagedApplications function
author: windows-sdk-content
description: The GetLocalManagedApplications function can be run on the target computer to get a list of managed applications on that computer.
old-location: policy\getlocalmanagedapplications.htm
tech.root: Policy
ms.assetid: 4606ff09-7e23-4953-aeef-cac822995d35
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetLocalManagedApplications, GetLocalManagedApplications function [Group Policy], appmgmt/GetLocalManagedApplications, policy.getlocalmanagedapplications
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
 - GetLocalManagedApplications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLocalManagedApplications function


## -description


The
    <b>GetLocalManagedApplications</b> function can be run on the target computer to get  a list of managed applications on that computer. The function can also be called in the context of a user to get a list of managed applications for that user. This function only returns applications that can be installed by the <a href="setup.windows_installer_start_page">Windows Installer</a>.


## -parameters




### -param bUserApps [in]

A value that, if <b>TRUE</b>, the <i>prgLocalApps</i> parameter contains a list of managed applications that applies to the user.  If the value of this parameter is <b>FALSE</b>, the <i>prgLocalApps</i> parameter contains a list of managed applications that applies to the local computer.


### -param pdwApps [out]

The address of a <b>DWORD</b> that specifies the number of applications in the list returned by <i>prgLocalApps</i>.


### -param prgLocalApps [out]

The address of an array that contains the list of managed applications. You must call <b>LocalFree</b> to free this array when its contents are no longer required. This parameter cannot be null. The list is returned as a <a href="https://msdn.microsoft.com/b2b7d209-76ee-4ba4-ac61-034d2c8e0689">LOCALMANAGEDAPPLICATION</a> structure.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b2b7d209-76ee-4ba4-ac61-034d2c8e0689">LOCALMANAGEDAPPLICATION</a>
 

 

