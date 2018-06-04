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

# SHILCreateFromPath function


## -description


<p class="CCE_Message">[<b>SHILCreateFromPath</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications should use <a href="https://msdn.microsoft.com/7bdfeed5-dcd0-40f6-a9d0-08ce816ee055">SHParseDisplayName</a> instead]

Creates a pointer to an item identifier list (PIDL) from a path.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH containing the path to be converted.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The path in <i>pszPath</i> expressed as a PIDL.


### -param rgfInOut

TBD




#### - rgflnOut [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that, on entry, indicates any attributes of the folder named in <i>pszPath</i> that the calling application would like to retrieve along with the PIDL. On exit, this value contains those requested attributes. For a list of possible attribute flags for this parameter, see <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



