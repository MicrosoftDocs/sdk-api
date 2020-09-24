---
UID: NF:userenv.GetProfileType
title: GetProfileType function (userenv.h)
description: Retrieves the type of profile loaded for the current user.
helpviewer_keywords: ["GetProfileType","GetProfileType function [Windows Shell]","PT_MANDATORY","PT_ROAMING","PT_ROAMING_PREEXISTING","PT_TEMPORARY","_shell_GetProfileType","shell.GetProfileType","userenv/GetProfileType"]
old-location: shell\GetProfileType.htm
tech.root: shell
ms.assetid: 55ee76c8-1735-43eb-a98e-9e6c87ee1ba7
ms.date: 12/05/2018
ms.keywords: GetProfileType, GetProfileType function [Windows Shell], PT_MANDATORY, PT_ROAMING, PT_ROAMING_PREEXISTING, PT_TEMPORARY, _shell_GetProfileType, shell.GetProfileType, userenv/GetProfileType
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProfileType
 - userenv/GetProfileType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - GetProfileType
---

# GetProfileType function


## -description

Retrieves the type of profile loaded for the current user.

## -parameters

### -param dwFlags [out]

Type: <b>DWORD*</b>

Pointer to a variable that receives the profile type. If the function succeeds, it sets one or more of the following values:



#### PT_MANDATORY

The user has a <a href="/previous-versions/windows/desktop/legacy/bb776895(v=vs.85)">Mandatory User Profiles</a>.



#### PT_ROAMING

The user has a <a href="/previous-versions/windows/desktop/legacy/bb776897(v=vs.85)">Roaming User Profiles</a>.



#### PT_ROAMING_PREEXISTING

The user has a <a href="/previous-versions/windows/desktop/legacy/bb776897(v=vs.85)">Roaming User Profile</a> that was created on another PC and is being downloaded.
						This profile type implies <b>PT_ROAMING</b>.
					



#### PT_TEMPORARY

The user has a <a href="/previous-versions/windows/desktop/legacy/bb776898(v=vs.85)">Temporary User Profiles</a>; it will be deleted at logoff.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the user profile is not already loaded, the function fails.

Note that the caller must have <b>KEY_READ</b> access to <b>HKEY_LOCAL_MACHINE</b>. This access right is granted by default. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

If the profile type is <b>PT_ROAMING_PREEXISTING</b>, Explorer will not reinitialize default programs associations when a profile is loaded on a machine for the first time.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>