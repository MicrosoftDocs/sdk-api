---
UID: NF:shlobj_core.SHGetFolderPathW
title: SHGetFolderPathW function
author: windows-sdk-content
description: Deprecated.
old-location: shell\SHGetFolderPath.htm
old-project: shell
ms.assetid: a240abc0-e0a6-4f95-8e74-7dc410970212
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: SHGFP_TYPE_CURRENT, SHGFP_TYPE_DEFAULT, SHGetFolderPath, SHGetFolderPath function [Windows Shell], SHGetFolderPathA, SHGetFolderPathW, _win32_SHGetFolderPath, _win32_SHGetFolderPath_cpp, shell.SHGetFolderPath, shlobj_core/SHGetFolderPath, shlobj_core/SHGetFolderPathA, shlobj_core/SHGetFolderPathW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetFolderPathW (Unicode) and SHGetFolderPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
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
 - bcrypt.dll
api_name:
 - SHGetFolderPath
 - SHGetFolderPathA
 - SHGetFolderPathW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHGetFolderPathW function


## -description


Deprecated. Gets the path of a folder identified by a <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value.
            
            
<div class="alert"><b>Note</b>  As of Windows Vista, this function is merely a wrapper for <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a>. The CSIDL value is translated to its associated <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> and then <b>SHGetKnownFolderPath</b> is called. New applications should use the known folder system rather than the older CSIDL system, which is supported only for backward compatibility.</div><div> </div>

## -parameters




### -param hwnd

TBD


### -param csidl

TBD


### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a> that can be used to represent a particular user. 
    
                        

<b>Microsoft Windows 2000 and earlier:</b> Always set this parameter to <b>NULL</b>.

<b>Windows XP and later:</b> This parameter is usually set to <b>NULL</b>, but you might need to assign a non-<b>NULL</b> value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.

The calling process is responsible for correct impersonation when <i>hToken</i> is non-<b>NULL</b>. The calling process must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This enables clients of <b>SHGetFolderPath</b> to find folder locations (such as the Desktop folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as My Documents and Desktop. Any items added to the Default User folder also appear in any new user account.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify the path to be returned. This value is used in cases where the folder associated with a <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> (or <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a>) can be moved, renamed, redirected, or roamed across languages by a user or administrator. 
    
                        

The known folder system that underlies <b>SHGetFolderPath</b> allows users or administrators to redirect a known folder to a location that suits their needs. This is achieved by calling <a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">IKnownFolderManager::Redirect</a>, which sets the "current" value of the folder associated with the SHGFP_TYPE_CURRENT flag.

The default value of the folder, which is the location of the folder if a user or administrator had not redirected it elsewhere, is retrieved by specifying the SHGFP_TYPE_DEFAULT flag. This value can be used to implement a "restore defaults" feature for a known folder.

For example, the default value (SHGFP_TYPE_DEFAULT) for <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_Music</a> (<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_MYMUSIC</a>) is "C:\Users\<b>user name</b>\Music". If the folder was redirected, the current value (SHGFP_TYPE_CURRENT) might be "D:\Music". If the folder has not been redirected, then SHGFP_TYPE_DEFAULT and SHGFP_TYPE_CURRENT retrieve the same path.



#### SHGFP_TYPE_CURRENT

Retrieve the folder's current path.



#### SHGFP_TYPE_DEFAULT

Retrieve the folder's default path.


### -param pszPath [out]

Type: <b>LPTSTR</b>

A pointer to a <b>null</b>-terminated string of length MAX_PATH which will receive the path. If an error occurs or S_FALSE is returned, this string will be empty. The returned path does not include a trailing backslash. For example, "C:\Users" is returned rather than "C:\Users\".


##### - dwFlags.SHGFP_TYPE_CURRENT

Retrieve the folder's current path.


##### - dwFlags.SHGFP_TYPE_DEFAULT

Retrieve the folder's default path.


#### - hwndOwner [in]

Type: <b>HWND</b>

Reserved.


#### - nFolder [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that identifies the folder whose path is to be retrieved. Only real folders are valid. If a virtual folder is specified, this function fails. You can force creation of a folder by combining the folder's <b>CSIDL</b> with <b>CSIDL_FLAG_CREATE</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is a superset of <a href="https://msdn.microsoft.com/4c39fdc1-5e43-4042-8703-fb72c88e2637">SHGetSpecialFolderPath</a>.

Only some <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> values are supported, including the following:

				

<ul>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_ADMINTOOLS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_APPDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_COMMON_ADMINTOOLS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_COMMON_APPDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_COMMON_DOCUMENTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_COOKIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_FLAG_CREATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_FLAG_DONT_VERIFY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_HISTORY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_INTERNET_CACHE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_LOCAL_APPDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_MYPICTURES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_PERSONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_PROGRAM_FILES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_PROGRAM_FILES_COMMON</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_SYSTEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_WINDOWS</a>
</li>
</ul>

#### Examples

The following code example uses <b>SHGetFolderPath</b> to find or create a folder and then creates a file in it.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>TCHAR szPath[MAX_PATH];

if(SUCCEEDED(SHGetFolderPath(NULL, 
                             CSIDL_PERSONAL|CSIDL_FLAG_CREATE, 
                             NULL, 
                             0, 
                             szPath))) 
{
    PathAppend(szPath, TEXT("New Doc.txt"));
    HANDLE hFile = CreateFile(szPath, ...);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1786db0-9bcc-4fc8-ae18-8519da6edda9">IKnownFolder::GetPath</a>
 

 

