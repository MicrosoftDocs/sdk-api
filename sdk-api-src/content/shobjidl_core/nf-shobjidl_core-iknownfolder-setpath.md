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

# IKnownFolder::SetPath


## -description


Assigns a new path to a known folder.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Either zero or the following value:



#### KF_FLAG_DONT_UNEXPAND

Set the full path without environment strings. If this flag is not set, portions of the path at <i>pszPath</i> may be represented by environment strings such as <code>%USERPROFILE%</code>.


### -param pszPath [in]

Type: <b>LPCWSTR</b>

Pointer to the folder's new path. This is a null-terminated Unicode string of length MAX_PATH. This path cannot be of zero length. If this value is <b>NULL</b>, the <b>IKnownFolder::SetPath</b> sets the path to the default value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method cannot be called on folders of type <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_FIXED</a> or <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_VIRTUAL</a>.

To call this method on a folder of type <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY_COMMON</a>, the calling application must be running with elevated privileges.

This method is equivalent to <a href="https://msdn.microsoft.com/b5758086-93d1-49d6-b9ac-ba8927f3bd1e">SHSetKnownFolderPath</a>.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/b5758086-93d1-49d6-b9ac-ba8927f3bd1e">SHSetKnownFolderPath</a>
 

 

