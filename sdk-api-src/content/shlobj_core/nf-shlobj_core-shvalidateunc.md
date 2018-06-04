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

# SHValidateUNC function


## -description


<p class="CCE_Message">[<b>SHValidateUNC</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Validates a Universal Naming Convention (UNC) path by calling <a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>. The function makes it possible for the user to type a remote network access (RNA) UNC application or document name from the <b>Run</b> dialog box on the <b>Start</b> menu.


## -parameters




### -param hwndOwner [in, optional]

Type: <b>HWND</b>

Handle of the parent window, used to display UI. If this is not needed, this value can be set to <b>NULL</b>.


### -param pszFile [in, out]

Type: <b>PWSTR</b>

A pointer to a null-terminated Unicode string that specifies the UNC path to validate. Note: This string must not be a constant string.


### -param fConnect

Type: <b>UINT</b>

One or more of the following values.



#### VALIDATEUNC_CONNECT (0x0001)

Connect a drive letter. When this flag is set, the value in <i>pszFile</i> is changed to the local drive to which the UNC is mapped on the local machine.



#### VALIDATEUNC_NOUI (0x0002)

On either failure or success, display no UI.



#### VALIDATEUNC_PRINT (0x0004)

Validate as a print share rather than disk share.



#### VALIDATEUNC_PERSIST (0x0008)

<b>Windows Vista and later</b>. The connection should be made persistent.



#### VALIDATEUNC_VALID

Mask value used to verify that the flags passed to <b>SHValidateUNC</b> are valid.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the UNC path exists; <b>FALSE</b> if the UNC path does not exist or if some other failure occurred.



