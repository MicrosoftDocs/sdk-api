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

# SHPathPrepareForWriteA function


## -description


Checks to see if the path exists. This includes remounting mapped network drives, prompting for ejectable media to be reinserted, creating the paths, prompting for the media to be formatted, and providing the appropriate user interfaces, if necessary. Read/write permissions for the medium are not checked.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to a window that specifies the parent window to be used for any user interface windows that must be created. If set to <b>NULL</b>, user interface windows are not created.


### -param punkEnableModless [in, optional]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>

A pointer to an <a href="_com_iunknown">IUnknown</a> interface that specifies the <a href="_ole_ioleinplaceactiveobject">IOleInPlaceActiveObject</a> object that implements the <a href="_ole_ioleinplaceactiveobject_enablemodeless">EnableModeless</a> method.


### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that specifies the path to be verified as valid for writing. This can be a UNC or file drive path.


### -param dwFlags

Type: <b>DWORD</b>

Flags that determine behavior options. This parameter can be a combination of the following values.



#### SHPPFW_NONE

Do not create new directories.



#### SHPPFW_DEFAULT

Default. Do not prompt the user if a directory needs to be created. This is identical to <b>SHPPFW_DIRCREATE</b>. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.



#### SHPPFW_DIRCREATE

Create directories without prompting the user. Do not pass with <b>SHPPFW_ASKDIRCREATE</b>.



#### SHPPFW_ASKDIRCREATE

Prompt the user before creating directories. Do not pass with <b>SHPPFW_DIRCREATE</b>.



#### SHPPFW_IGNOREFILENAME

Last item in <i>pszPath</i> is a file name, so ignore. For example, if <i>pszPath</i>="C:\MyDir\MyFile.doc", only use "C:\MyDir". If <i>pszPath</i>="C:\MyFirDir\MySecDir", only use "C:\MyFirDir".



#### SHPPFW_NOWRITECHECK

Not currently implemented.



#### SHPPFW_MEDIACHECKONLY

<b>Windows XP or later.</b> Suppresses the "not accessible" error message box, which displays when a failure other than a user cancellation occurs, and <i>hwnd</i> is not <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the path is available, or an error code otherwise. Note that a return value of S_OK does not mean that the medium is writable; it simply means that the path is available.




## -remarks



The primary use of this function is for a program to check a path before using it and display the necessary user interface to prompt the user. For example, if the disk in drive A: were missing, a window that prompts the user to insert the disk would appear.



