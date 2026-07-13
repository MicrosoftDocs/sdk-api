---
UID: NF:userenv.CreateAppContainerProfile
title: CreateAppContainerProfile function (userenv.h)
description: Creates a per-user, per-app profile for an AppContainer.
helpviewer_keywords: ["CreateAppContainerProfile","CreateAppContainerProfile function [Windows Shell]","shell.createappcontainerprofile","userenv/CreateAppContainerProfile"]
old-location: shell\createappcontainerprofile.htm
tech.root: shell
ms.assetid: 73F5F30F-4083-4D33-B181-31B782AD40D6
ms.date: 11/26/2024
ms.keywords: CreateAppContainerProfile, CreateAppContainerProfile function [Windows Shell], shell.createappcontainerprofile, userenv/CreateAppContainerProfile
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - CreateAppContainerProfile
 - userenv/CreateAppContainerProfile
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
 - CreateAppContainerProfile
---

## -description

Creates a per-user, per-app profile for an AppContainer.

## -parameters

### -param pszAppContainerName [in]

The name of the app container. To ensure uniqueness, this string should ideally contain the app name as well as the publisher. This string can be up to 64 characters in length. Further, it must fit into the pattern described by the regular expression "[-_. A-Za-z0-9]+".

### -param pszDisplayName [in]

The display name. This string can be up to 512 characters in length.

### -param pszDescription [in]

A description for the app container. This string can be up to 2048 characters in length.

### -param pCapabilities [in]

The SIDs that define the requested UWP capabilities (if applicable).

### -param dwCapabilityCount [in]

The number of SIDs in *pCapabilities*.

### -param ppSidAppContainerSid [out]

The SID for the profile. This buffer must be freed using the [FreeSid](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) function.

## -returns

If this function succeeds, then it returns a standard HRESULT code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The data store was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller doesn't have permission to create the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The application data store already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The container name is <b>NULL</b>, or the container name, the display name, or the description strings exceed their specified respective limits for length.

</td>
</tr>
</table>

## -remarks

A profile contains folders and registry storage that are per-user and per-app. The folders have ACLs that prevent them from being accessed by other users and apps. These folders can be accessed by calling [SHGetKnownFolderPath](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath).

The function creates a profile for the current user. To create a profile on behalf of another user, you must impersonate that user. To create profiles for multiple users of the same app, you must call **CreateAppContainerProfile** for each user.

## -see-also

* [DeleteAppContainerProfile](/windows/win32/api/userenv/nf-userenv-deleteappcontainerprofile)
