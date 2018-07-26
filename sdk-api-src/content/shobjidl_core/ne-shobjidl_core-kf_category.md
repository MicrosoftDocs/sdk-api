---
UID: NE:shobjidl_core.KF_CATEGORY
title: KF_CATEGORY
author: windows-sdk-content
description: Value that represent a category by which a folder registered with the Known Folder system can be classified.
old-location: shell\KF_CATEGORY.htm
old-project: shell
ms.assetid: 2ca0d3e2-bb4c-4a28-90d6-fe2852373b88
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: KF_CATEGORY, KF_CATEGORY enumeration [Windows Shell], KF_CATEGORY_COMMON, KF_CATEGORY_FIXED, KF_CATEGORY_PERUSER, KF_CATEGORY_VIRTUAL, _shell_KF_CATEGORY, shell.KF_CATEGORY, shobjidl_core/KF_CATEGORY, shobjidl_core/KF_CATEGORY_COMMON, shobjidl_core/KF_CATEGORY_FIXED, shobjidl_core/KF_CATEGORY_PERUSER, shobjidl_core/KF_CATEGORY_VIRTUAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: KF_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - KF_CATEGORY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# KF_CATEGORY enumeration


## -description


Value that represent a category by which a folder registered with the Known Folder system can be classified.


## -enum-fields




### -field KF_CATEGORY_VIRTUAL

Virtual folders are not part of the file system, which is to say that they have no path. For example, <b>Control Panel</b> and <b>Printers</b> are virtual folders. A number of features such as folder path and redirection do not apply to this category.


### -field KF_CATEGORY_FIXED

Fixed file system folders are not managed by the Shell and are usually given a permanent path when the system is installed. For example, the <b>Windows</b> and <b>Program Files</b> folders are fixed folders. A number of features such as redirection do not apply to this category.


### -field KF_CATEGORY_COMMON

Common folders are those file system folders used for sharing data and settings, accessible by all users of a system. For example, all users share a common <b>Documents</b> folder as well as their per-user <b>Documents</b> folder.


### -field KF_CATEGORY_PERUSER

Per-user folders are those stored under each user's profile and accessible only by that user. For example, <code>%USERPROFILE%\Pictures</code>. This category of folder usually supports many features including aliasing, redirection and customization. 
                
                



<div class="alert"><b>Note</b>  The user profile root folder (<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_Profile</a>) does not support redirection.</div>
<div> </div>

## -remarks



The <b>KF_CATEGORY</b> type is defined in Shobjidl.h as shown here.

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef DWORD KF_CATEGORY;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b3a7f249-9d57-4bd1-830f-1c83c745782f">IKnownFolder::GetCategory</a>



<a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

