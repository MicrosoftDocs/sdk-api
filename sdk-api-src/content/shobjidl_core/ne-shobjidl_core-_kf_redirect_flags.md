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

# _KF_REDIRECT_FLAGS enumeration


## -description


Flags used by <a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">IKnownFolderManager::Redirect</a> to specify details of a known folder redirection such as permissions and ownership for the redirected folder.


## -enum-fields




### -field KF_REDIRECT_USER_EXCLUSIVE

Ensure that only the user has permission to access the redirected folder.


### -field KF_REDIRECT_COPY_SOURCE_DACL

Copy the DACL of the source folder to the target to maintain current access permissions.


### -field KF_REDIRECT_OWNER_USER

Sets the user as the owner of a newly created target folder unless the user is a member of the Administrator group, in which case Administrator is set as the owner. Must be called with KF_REDIRECT_SET_OWNER_EXPLICIT.


### -field KF_REDIRECT_SET_OWNER_EXPLICIT

Set the owner of a newly created target folder.  If the user belongs to the Administrators group, Administrators is assigned as the owner. Must be called with KF_REDIRECT_OWNER_USER.


### -field KF_REDIRECT_CHECK_ONLY

Do not perform a redirection, simply check whether redirection has occurred. If so, <a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">IKnownFolderManager::Redirect</a> returns S_OK; if not, or if some actions remain to be completed, it returns S_FALSE.


### -field KF_REDIRECT_WITH_UI

Display UI during the redirection.


### -field KF_REDIRECT_UNPIN

Unpin the source folder.


### -field KF_REDIRECT_PIN

Pin the target folder.


### -field KF_REDIRECT_COPY_CONTENTS

Copy the existing contents—both files and subfolders—of the known folder to the redirected folder.


### -field KF_REDIRECT_DEL_SOURCE_CONTENTS

Delete the contents of the source folder after they have been copied to the redirected folder. This flag is valid only if <a href="https://msdn.microsoft.com/6016f02f-5480-4fd8-b21d-209ebd863922">KF_REDIRECT_COPY_CONTENTS</a> is set.


### -field KF_REDIRECT_EXCLUDE_ALL_KNOWN_SUBFOLDERS

Reserved. Do not use.


## -remarks



The <b><b>KF_REDIRECT_OWNER_USER</b></b> and <b><b>KF_REDIRECT_SET_OWNER_EXPLICIT</b></b> flags provide ownership checks for the target folder, if that folder exists. By default, <a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">IKnownFolderManager::Redirect</a> does not perform ownership checks. KF_REDIRECT_OWNER_USER and KF_REDIRECT_SET_OWNER_EXPLICIT are only valid if called together.

The <b>KF_REDIRECT_FLAGS</b> type is defined in Shobjidl.h as shown here.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef DWORD KF_REDIRECT_FLAGS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

