---
UID: NF:userenv.DeleteProfileA
title: DeleteProfileA function (userenv.h)
author: windows-sdk-content
description: Deletes the user profile and all user-related settings from the specified computer. The caller must have administrative privileges to delete a user's profile.
old-location: shell\DeleteProfile.htm
tech.root: shell
ms.assetid: 48a08d9a-4fdc-43ab-8323-c49bc2d0a58d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteProfile, DeleteProfile function [Windows Shell], DeleteProfileA, DeleteProfileW, _shell_DeleteProfile, shell.DeleteProfile, userenv/DeleteProfile, userenv/DeleteProfileA, userenv/DeleteProfileW
ms.topic: function
f1_keywords: 
 - "userenv/DeleteProfile"
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteProfileW (Unicode) and DeleteProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - DeleteProfile
 - DeleteProfileA
 - DeleteProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteProfileA function


## -description


Deletes the user profile and all user-related settings from the specified computer. The caller must have administrative privileges to delete a user's profile.


## -parameters




### -param lpSidString [in]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the user 
    <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-identifiers">SID</a>.


### -param lpProfilePath [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the profile path. If this parameter is <b>NULL</b>, the function obtains the path from the registry.


### -param lpComputerName [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a string that specifies the name of the computer from which the profile is to be deleted. If this parameter is <b>NULL</b>, the local computer name is used.
    
                        

<div class="alert"><b>Note</b>  As of Windows Vista, this parameter must be <b>NULL</b>. If it is not, this function fails with the error code ERROR_INVALID_PARAMETER.</div>
<div> </div>

## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<b>DeleteProfile</b> might fail when passed the security identifier (SID) of the local system account (S-1-5-18). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=200321">KB890212</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
 

 

