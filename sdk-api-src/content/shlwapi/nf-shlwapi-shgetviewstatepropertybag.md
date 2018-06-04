---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Allows the property bag to roam. See <a href="https://msdn.microsoft.com/8af06fdf-be99-4295-8f11-7d7f68e66956">Roaming User Profiles</a>. This flag cannot be combined with SHGVSPB_ALLFOLDERS.



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

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Critical information should not be stored in the view state property bag because the system keeps only a limited number of view states. If a folder is not visited for a long time, its view state is eventually deleted.

We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.



