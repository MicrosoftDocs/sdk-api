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

# SHStartNetConnectionDialogA function


## -description


<p class="CCE_Message">[<b>SHStartNetConnectionDialog</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a general browsing dialog box for a network resource connection.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.


### -param pszRemoteName [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated character string that specifies the remote network name. This value can be set to <b>NULL</b>.


### -param dwType

Type: <b>DWORD</b>

A bitfield that contains a set of flags that identify the type of resource that the dialog box is set to find. This value can contain one of the following values, defined in Winnetwk.h:



#### RESOURCETYPE_ANY (0x00000000)

All resources



#### RESOURCETYPE_DISK (0x00000001)

Disk resources



#### RESOURCETYPE_PRINT (0x00000002)

Print resources


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



