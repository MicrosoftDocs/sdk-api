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

# CreateAppContainerProfile function


## -description


Creates a per-user, per-app profile for Windows Store apps.


## -parameters




### -param pszAppContainerName [in]

The name of the app container. To ensure uniqueness, it is recommended that this string contains the app name as well as the publisher. This string can be up to 64 characters in length.  Further, it must fit into the pattern described by the regular expression "[-_. A-Za-z0-9]+". 


### -param pszDisplayName [in]

The display name. This string can be up to 512 characters in length.


### -param pszDescription [in]

A description for the app container. This string can be up to 2048 characters in length.


### -param pCapabilities [in]

The SIDs that define the requested capabilities.


### -param dwCapabilityCount [in]

The number of SIDs in <i>pCapabilities</i>.


### -param ppSidAppContainerSid [out]

The SID for the profile. This buffer must be freed using the <a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a> function.


## -returns



If this function succeeds, it returns a standard HRESULT code, including the following:

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
The caller does not have permission to create the profile.

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
The container name   is <b>NULL</b>,  or the container name,   the display name, or the description strings exceed their specified respective limits for length.

</td>
</tr>
</table>
 




## -remarks



A profile contains folders and registry storage that are per-user and per-app. The folders have ACLs that prevent them from being accessed by other users and apps. These folders can be accessed by calling <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a>.

The function creates a profile for the current user. To create a profile on behalf of another user, you must impersonate that user. To create profiles for multiple users of the same app, you must call <b>CreateAppContainerProfile</b> for each user.




## -see-also




<a href="https://msdn.microsoft.com/ED79D661-D087-4E44-8C32-14705ACA9D40">DeleteAppContainerProfile</a>
 

 

