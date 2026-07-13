---
UID: NF:shlwapi.SHGetViewStatePropertyBag
title: SHGetViewStatePropertyBag function (shlwapi.h)
description: SHGetViewStatePropertyBag may be altered or unavailable.
helpviewer_keywords: ["SHGVSPB_ALLFOLDERS","SHGVSPB_ALLUSERS","SHGVSPB_FOLDER","SHGVSPB_FOLDERNODEFAULTS","SHGVSPB_GLOBALDEFAULTS","SHGVSPB_INHERIT","SHGVSPB_NOAUTODEFAULTS","SHGVSPB_PERFOLDER","SHGVSPB_PERUSER","SHGVSPB_ROAM","SHGVSPB_USERDEFAULTS","SHGetViewStatePropertyBag","SHGetViewStatePropertyBag function [Windows Shell]","shell.SHGetViewStatePropertyBag","shell_SHGetViewStatePropertyBag","shlwapi/SHGetViewStatePropertyBag"]
old-location: shell\SHGetViewStatePropertyBag.htm
tech.root: shell
ms.assetid: 6852867a-30a5-4d4e-b790-3746104e3ed8
ms.date: 12/05/2018
ms.keywords: SHGVSPB_ALLFOLDERS, SHGVSPB_ALLUSERS, SHGVSPB_FOLDER, SHGVSPB_FOLDERNODEFAULTS, SHGVSPB_GLOBALDEFAULTS, SHGVSPB_INHERIT, SHGVSPB_NOAUTODEFAULTS, SHGVSPB_PERFOLDER, SHGVSPB_PERUSER, SHGVSPB_ROAM, SHGVSPB_USERDEFAULTS, SHGetViewStatePropertyBag, SHGetViewStatePropertyBag function [Windows Shell], shell.SHGetViewStatePropertyBag, shell_SHGetViewStatePropertyBag, shlwapi/SHGetViewStatePropertyBag
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetViewStatePropertyBag
 - shlwapi/SHGetViewStatePropertyBag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHGetViewStatePropertyBag
---

# SHGetViewStatePropertyBag function


## -description

<p class="CCE_Message">[<b>SHGetViewStatePropertyBag</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a property bag in which the view state information for a folder can be stored and subsequently retrieved. The user's settings are kept for the next time the user visits the folder.

## -parameters

### -param pidl [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL of the folder for which you are requesting properties. This parameter must be <b>NULL</b> if the SHGVSPB_ALLFOLDERS flag is passed.

### -param pszBagName [in, optional]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the requested property bag.

### -param dwFlags

Type: <b>DWORD</b>

A value that specifies a combination of the following flags.


One value from the following set of flags is required.





#### SHGVSPB_PERUSER

Returns the per-user properties for the specified <i>pidl</i>.



#### SHGVSPB_ALLUSERS

Returns the All User properties for the specified <i>pidl</i>.


One value from the following set of flags is required.





#### SHGVSPB_PERFOLDER

Returns the property bag for the folder specified by the <i>pidl</i> parameter.



#### SHGVSPB_ALLFOLDERS

Returns the property bag that applies to all folders.



#### SHGVSPB_INHERIT

Returns the property bag used to provide defaults for subfolders that do not have their property bag.


The following flags are optional.





#### SHGVSPB_ROAM

Allows the property bag to roam. See <a href="/previous-versions/windows/desktop/legacy/bb776897(v=vs.85)">Roaming User Profiles</a>. This flag cannot be combined with SHGVSPB_ALLFOLDERS.



#### SHGVSPB_NOAUTODEFAULTS

Suppresses the search for a suitable default when the property bag cannot be found for the specified folder. By default, if SHGVSPB_INHERIT is not specified and a property bag cannot be found for the specified folder, the system searches for identically named property bags in other locations that may be able to provide default values. For example, the system searches in the ancestors of the folder to see if any of them provide a SHGVSPB_INHERIT property bag. Other places the system searches are in the user defaults and the global defaults.


The following set of flags consists of values that combine some flags listed above, and are used for brevity and convenience.





#### SHGVSPB_FOLDER

Combines SHGVSPB_PERUSER and SHGVSPB_PERFOLDER.



#### SHGVSPB_FOLDERNODEFAULTS

Combines SHGVSPB_PERUSER, SHGVSPB_PERFOLDER, and SHGVSPB_NOAUTODEFAULTS.



#### SHGVSPB_USERDEFAULTS

Combines SHGVSPB_PERUSER and SHGVSPB_ALLFOLDERS.



#### SHGVSPB_GLOBALDEFAULTS

Combines SHGVSPB_ALLUSERS and SHGVSPB_ALLFOLDERS.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is named SHGVSPB_GLOBALDEAFAULTS.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Critical information should not be stored in the view state property bag because the system keeps only a limited number of view states. If a folder is not visited for a long time, its view state is eventually deleted.

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.