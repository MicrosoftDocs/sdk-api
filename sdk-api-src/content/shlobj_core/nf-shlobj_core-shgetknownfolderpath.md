---
UID: NF:shlobj_core.SHGetKnownFolderPath
title: SHGetKnownFolderPath function
author: windows-sdk-content
description: Retrieves the full path of a known folder identified by the folder's KNOWNFOLDERID.
old-location: shell\SHGetKnownFolderPath.htm
old-project: shell
ms.assetid: 5434c744-484b-4c34-9a76-dddbcb81eb29
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHGetKnownFolderPath, SHGetKnownFolderPath function [Windows Shell], _shell_SHGetKnownFolderPath, shell.SHGetKnownFolderPath, shlobj_core/SHGetKnownFolderPath
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	API-MS-Win-shell-shellfolders-l1-1-0.dll
-	KernelBase.dll
-	Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
-	Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
-	Windows.Storage.dll
api_name:
-	SHGetKnownFolderPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHGetKnownFolderPath function


## -description


Retrieves the full path of a known folder identified by the folder's <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that identifies the folder.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KNOWN_FOLDER_FLAG</a> values.


### -param hToken [in, optional]

Type: <b>HANDLE</b>

An <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a> that represents a particular user. If this parameter is <b>NULL</b>, which is the most common usage, the function requests the known folder for the current user. 
    
                        

Request a specific user's folder by passing the <i>hToken</i> of that user. This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user. That token must be opened with <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">TOKEN_QUERY</a> and <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">TOKEN_IMPERSONATE</a> rights. In some cases, you also need to include <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">TOKEN_DUPLICATE</a>. In addition to passing the user's <i>hToken</i>, the registry hive of that specific user must be mounted. See <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHGetKnownFolderPath</b> to find folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.


### -param ppszPath [out]

Type: <b>PWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that specifies the path of the known folder. The calling process is responsible for freeing this resource once it is no longer needed by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. The returned path does not include a trailing backslash. For example, "C:\Users" is returned rather than "C:\Users\".


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> which does not have a path (such as a folder marked as <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_VIRTUAL</a>).

</td>
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



This function replaces <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a>. That older function is now simply a wrapper for <b>SHGetKnownFolderPath</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1786db0-9bcc-4fc8-ae18-8519da6edda9">IKnownFolder::GetPath</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/fed9cfb8-4c38-4947-99aa-278245148136">SHGetKnownFolderIDList</a>



<a href="https://msdn.microsoft.com/b5758086-93d1-49d6-b9ac-ba8927f3bd1e">SHSetKnownFolderPath</a>
 

 

