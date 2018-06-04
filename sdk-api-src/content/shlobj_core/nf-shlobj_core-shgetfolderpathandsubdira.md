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

# SHGetFolderPathAndSubDirA function


## -description


Gets the path of a folder and appends a user-provided subfolder path.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

Reserved.


### -param csidl [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that identifies the folder whose path is to be retrieved. Only real folders are valid. If a virtual folder is specified, this function fails. You can force creation of a folder with <b>SHGetFolderPathAndSubDir</b> by combining the folder's <b>CSIDL</b> with CSIDL_FLAG_CREATE.


### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="https://msdn.microsoft.com/350159c9-2399-427a-ba44-c897a9664299">access token</a> that represents a particular user. For systems earlier than Windows 2000, set this value to <b>NULL</b>. For later systems, <i>hToken</i> is usually, but not always, set to <b>NULL</b>. You might need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <a href="https://msdn.microsoft.com/d9ffda6f-adc0-44a3-b410-e23bf5f4f165">My Documents</a>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Specifies whether the path to be returned is the actual path of the folder or the default path. This value is used in cases where the folder associated with a <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value may be moved or renamed by the user.



#### SHGFP_TYPE_CURRENT

Return the folder's current path.



#### SHGFP_TYPE_DEFAULT

Return the folder's default path.


### -param pszSubDir [in]

Type: <b>LPCTSTR</b>

A pointer to the subpath to be appended to the folder's path. This is a <b>null</b>-terminated string of length MAX_PATH. If you are not creating a new directory, this must be an existing subdirectory or the function returns an error. This value can be <b>NULL</b> if no subpath is to be appended.


### -param pszPath [out]

Type: <b>LPTSTR</b>

When this function returns, this value points to the directory path and appended subpath. This is a <b>null</b>-terminated string of length MAX_PATH. This string is empty when the function returns an error code.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a>
 

 

