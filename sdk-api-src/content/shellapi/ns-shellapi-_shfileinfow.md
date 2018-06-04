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

# _SHFILEINFOW structure


## -description


Contains information about a file object.


## -struct-fields




### -field hIcon

Type: <b>HICON</b>

A handle to the icon that represents the file. You are responsible for destroying this handle with <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> when you no longer need it.


### -field iIcon

Type: <b>int</b>

The index of the icon image within the system image list.


### -field dwAttributes

Type: <b>DWORD</b>

An array of values that indicates the attributes of the file object. For information about these values, see the <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a> method.


### -field szDisplayName

Type: <b>TCHAR[MAX_PATH]</b>

A string that contains the name of the file as it appears in the Windows Shell, or the path and file name of the file that contains the icon representing the file.


### -field szTypeName

Type: <b>TCHAR[80]</b>

A string that describes the type of file.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a> function.



