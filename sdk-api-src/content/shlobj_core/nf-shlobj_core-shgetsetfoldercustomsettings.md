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

# SHGetSetFolderCustomSettings function


## -description


<p class="CCE_Message">[<b>SHGetSetFolderCustomSettings</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets or retrieves custom folder settings. This function reads from and writes to Desktop.ini.


## -parameters




### -param pfcs [in, out]

Type: <b>LPSHFOLDERCUSTOMSETTINGS</b>

A pointer to a <a href="https://msdn.microsoft.com/a6357372-80ef-4719-b53f-87eb3fdc1b0d">SHFOLDERCUSTOMSETTINGS</a> structure that provides or receives the custom folder settings.


### -param pszPath [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated Unicode string that contains the path to the folder. The length of  <b>pszPath</b> must be MAX_PATH or less, including the terminating null character.


### -param dwReadWrite

Type: <b>DWORD</b>

A flag that controls the action of the function. It may be one of the following values.



#### FCS_READ (0x00000001)

Retrieve the custom folder settings in <i>pfcs</i>.



#### FCS_FORCEWRITE (0x00000002)

Use <i>pfcs</i> to set the custom folder's settings regardless of whether the values are already present.



#### FCS_WRITE (FCS_READ | FCS_FORCEWRITE)

Use <i>pfcs</i> to set the custom folder's settings if the values are not already present.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only Unicode strings are supported.

<b>Windows Server 2003 and Windows XP:  </b><b>SHGetSetFolderCustomSettings</b> supports both ANSI and Unicode strings.



