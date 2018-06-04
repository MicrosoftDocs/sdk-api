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

# SHEmptyRecycleBinW function


## -description


Empties the Recycle Bin on the specified drive.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window of any dialog boxes that might be displayed during the operation. This parameter can be <b>NULL</b>.


### -param pszRootPath [in, optional]

Type: <b>LPCTSTR</b>

The address of a null-terminated string of maximum length MAX_PATH that contains the path of the root drive on which the Recycle Bin is located. This parameter can contain the address of a string formatted with the drive, folder, and subfolder names, for example c:\windows\system\. It can also contain an empty string or <b>NULL</b>. If this value is an empty string or <b>NULL</b>, all Recycle Bins on all drives will be emptied.


### -param dwFlags

Type: <b>DWORD</b>

One or more of the following values.



#### SHERB_NOCONFIRMATION

No dialog box confirming the deletion of the objects will be displayed.



#### SHERB_NOPROGRESSUI

No dialog box indicating the progress will be displayed.



#### SHERB_NOSOUND

No sound will be played when the operation is complete.


##### - dwFlags.SHERB_NOCONFIRMATION

No dialog box confirming the deletion of the objects will be displayed.


##### - dwFlags.SHERB_NOPROGRESSUI

No dialog box indicating the progress will be displayed.


##### - dwFlags.SHERB_NOSOUND

No sound will be played when the operation is complete.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a9a80486-2c99-4916-af25-10b00573456b">SHQueryRecycleBin</a>
 

 

