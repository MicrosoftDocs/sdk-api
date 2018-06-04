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

# EXP_SPECIAL_FOLDER structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds special folder information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the <b>EXP_SPECIAL_FOLDER</b> structure.


### -field dwSignature

Type: <b>DWORD</b>

The structure's signature. It should be set to EXP_SPECIAL_FOLDER_SIG.


### -field idSpecialFolder

Type: <b>DWORD</b>

The ID of the special folder that the link points into.


### -field cbOffset

Type: <b>DWORD</b>

The offset into the saved PIDL.

