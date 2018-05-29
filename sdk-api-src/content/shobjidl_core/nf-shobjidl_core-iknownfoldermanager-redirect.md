---
UID: NF:shobjidl_core.IKnownFolderManager.Redirect
title: IKnownFolderManager::Redirect
author: windows-sdk-content
description: Redirects folder requests for common and per-user folders.
old-location: shell\IKnownFolderManager_Redirect.htm
old-project: shell
ms.assetid: 0f4fc609-597b-4c72-b875-4b3f051dd056
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IKnownFolderManager interface [Windows Shell],Redirect method, IKnownFolderManager.Redirect, IKnownFolderManager::Redirect, Redirect, Redirect method [Windows Shell], Redirect method [Windows Shell],IKnownFolderManager interface, _shell_IKnownFolderManager_Redirect, shell.IKnownFolderManager_Redirect, shobjidl_core/IKnownFolderManager::Redirect
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IKnownFolderManager.Redirect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolderManager::Redirect


## -description


Redirects folder requests for common and per-user folders.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> of the folder to be redirected.


### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window used to display copy engine progress UI dialogs when <a href="https://msdn.microsoft.com/6016f02f-5480-4fd8-b21d-209ebd863922">KF_REDIRECT_WITH_UI</a> i passed in the <i>flags</i> parameter. If no progress dialog is needed, this value can be <b>NULL</b>.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/6016f02f-5480-4fd8-b21d-209ebd863922">KF_REDIRECT_FLAGS</a></b>

The <a href="https://msdn.microsoft.com/6016f02f-5480-4fd8-b21d-209ebd863922">KF_REDIRECT_FLAGS</a> options for redirection.


### -param pszTargetPath [in, optional]

Type: <b>LPCWSTR</b>

A pointer to the new path for the folder. This is a null-terminated Unicode string. This value can be <b>NULL</b>.


### -param cFolders [in]

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values in the array at <i>pExclusion</i>.


### -param pExclusion [in]

Type: <b>KNOWNFOLDERID const*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values that refer to subfolders of <i>rfid</i> that should be excluded from the redirection. If no subfolders are excluded, this value can be <b>NULL</b>.


### -param ppszError [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that contains an error message if one was generated. This value can be <b>NULL</b>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

