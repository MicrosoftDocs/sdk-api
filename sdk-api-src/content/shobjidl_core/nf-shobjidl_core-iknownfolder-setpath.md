---
UID: NF:shobjidl_core.IKnownFolder.SetPath
title: IKnownFolder::SetPath
author: windows-sdk-content
description: Assigns a new path to a known folder.
old-location: shell\IKnownFolder_SetPath.htm
tech.root: shell
ms.assetid: 235f69de-3571-4184-aa52-b409fbc1d643
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IKnownFolder interface [Windows Shell],SetPath method, IKnownFolder.SetPath, IKnownFolder::SetPath, KF_FLAG_DONT_UNEXPAND, SetPath, SetPath method [Windows Shell], SetPath method [Windows Shell],IKnownFolder interface, _shell_IKnownFolder_SetPath, shell.IKnownFolder_SetPath, shobjidl_core/IKnownFolder::SetPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder.SetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

