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

# _KF_DEFINITION_FLAGS enumeration


## -description


Flags that specify certain known folder behaviors. Used with the <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure.


## -enum-fields




### -field KFDF_LOCAL_REDIRECT_ONLY

Prevent a <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">per-user</a> known folder from being redirected to a network location. Note that if the known folder has been flagged with KFDF_LOCAL_REDIRECT_ONLY but it is a subfolder of a known folder that is redirected to a network location, this subfolder is redirected also.


### -field KFDF_ROAMABLE

Can be roamed through a PC-to-PC synchronization.


### -field KFDF_PRECREATE

Create the folder when the user first logs on. Normally a known folder is not created until it is first called. At that time, an API such as <a href="https://msdn.microsoft.com/dc75ee60-7319-4a11-949e-dd0c3deabd8f">SHCreateItemInKnownFolder</a> or <a href="https://msdn.microsoft.com/a42c0a20-9c72-48d3-8432-15b73ff211d2">IKnownFolder::GetShellItem</a> is called with the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KF_FLAG_CREATE</a> flag. However, some known folders need to exist immediately. An example is those known folders under %USERPROFILE%, which must exist to provide a proper view. In those cases, KFDF_PRECREATE is set and Windows Explorer calls the creation API during its user initialization.


### -field KFDF_STREAM

<b>Introduced in Windows 7</b>. The known folder is a file rather than a folder.


### -field KFDF_PUBLISHEXPANDEDPATH

<b>Introduced in Windows 7</b>. The full path of the known folder, with any environment variables fully expanded, is stored in the registry under HKEY_CURRENT_USER.


### -field KFDF_NO_REDIRECT_UI

<b>Introduced in Windows 8.1</b>. Prevent showing the <b>Locations</b> tab in the property dialog of the known folder. 

<b>Introduced in Windows 8.1</b>. Prevent showing the <b>Locations</b> tab in the property dialog of the known folder. 


## -remarks



The <b>KF_DEFINITION_FLAGS</b> type is defined in Shobjidl.h as shown here.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef DWORD KF_DEFINITION_FLAGS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

