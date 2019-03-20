---
UID: NF:shlobj_core.SHSetKnownFolderPath
title: SHSetKnownFolderPath function (shlobj_core.h)
author: windows-sdk-content
description: Redirects a known folder to a new location.
old-location: shell\SHSetKnownFolderPath.htm
tech.root: shell
ms.assetid: b5758086-93d1-49d6-b9ac-ba8927f3bd1e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: KF_FLAG_DONT_UNEXPAND, SHSetKnownFolderPath, SHSetKnownFolderPath function [Windows Shell], _shell_SHSetKnownFolderPath, shell.SHSetKnownFolderPath, shlobj_core/SHSetKnownFolderPath
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHSetKnownFolderPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHSetKnownFolderPath function


## -description


Redirects a known folder to a new location.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A <b>GUID</b> that identifies the known folder.


### -param dwFlags [in]

Type: <b>DWORD</b>

Either 0 or the following value.



#### KF_FLAG_DONT_UNEXPAND

If this flag is set, portions of the path referenced by <i>pszPath</i> may be represented by environment strings such as <code>%USERPROFILE%</code>.


### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a> used to represent a particular user. This parameter is usually set to <b>NULL</b>, in which case the function tries to access the current user's instance of the folder. However, you may need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.
			
            		

The calling application is responsible for correct impersonation when <i>hToken</i> is non-null. It must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHSetKnownFolderPath</b> to set folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.


### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to the folder's new path. This is a null-terminated Unicode string of length MAX_PATH. This path cannot be of zero length.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="https://msdn.microsoft.com/3ac09fc4-15c4-4346-94ad-2a4617c463d1">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values for the current system.

</td>
</tr>
</table>
 




## -remarks



This function replaces <a href="https://msdn.microsoft.com/9da142fa-4765-4889-bd4c-d8167a16f86b">SHSetFolderPath</a>. That older function is now simply a wrapper for <b>SHSetKnownFolderPath</b>.

The caller of this function must have Administrator privileges. To call this function on public known folders, the caller must have Administrator privileges. For per-user known folders the caller only requires User privileges.

Some of the known folders, for example, the <b>Documents</b> folder, are per-user. Every user has a different path for their <b>Documents</b> folder. If <i>hToken</i> is <b>NULL</b>, the API tries to access the calling application's instance of the folder, which is that of the current user. If <i>hToken</i> is a valid user token, the API tries to impersonate the user using this token and tries to access that user's instance.

This function cannot be called on folders of type <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_FIXED</a> and <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_VIRTUAL</a>.

To call this function on a folder of type <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_COMMON</a>, the calling application must be running with elevated privileges.




## -see-also




<a href="https://msdn.microsoft.com/c1786db0-9bcc-4fc8-ae18-8519da6edda9">IKnownFolder::GetPath</a>



<a href="https://msdn.microsoft.com/235f69de-3571-4184-aa52-b409fbc1d643">IKnownFolder::SetPath</a>



<a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">IKnownFolderManager::Redirect</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/fed9cfb8-4c38-4947-99aa-278245148136">SHGetKnownFolderIDList</a>



<a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a>
 

 

