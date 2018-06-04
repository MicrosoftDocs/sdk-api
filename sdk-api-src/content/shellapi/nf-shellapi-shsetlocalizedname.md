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

# SHSetLocalizedName function


## -description


Sets the localized name of a file in a Shell folder.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string that specifies the fully qualified path of the target file.


### -param pszResModule [in]

Type: <b>PCWSTR</b>

A pointer to a string resource that specifies the localized version of the file name.


### -param idsRes

Type: <b>int</b>

An integer ID that specifies the localized file name in the string resource.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this string is set, Explorer displays this string instead of the file name. The path to the file is unchanged.
                
                

Applications can get the display (localized) name with <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> with the <a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN_NORMALDISPLAY</a> flag and the parsing (non-localized) name with <a href="https://msdn.microsoft.com/9b159be9-3797-4c8b-90f8-9d3b3a3afb71">IShellItem::GetDisplayName</a> using the <a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN_DESKTOPABSOLUTEPARSING</a> flag.

Calling <a href="https://msdn.microsoft.com/ed30546f-3531-42df-9018-1a24a79a0b79">SHRemoveLocalizedName</a> makes the display name identical to the parsing name.



