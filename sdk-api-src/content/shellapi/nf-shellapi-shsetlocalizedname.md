---
UID: NF:shellapi.SHSetLocalizedName
title: SHSetLocalizedName function
author: windows-sdk-content
description: Sets the localized name of a file in a Shell folder.
old-location: shell\SHSetLocalizedName.htm
tech.root: shell
ms.assetid: 35b83fc8-3dad-4f08-a3fe-ce047b2ca3a2
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: SHSetLocalizedName, SHSetLocalizedName function [Windows Shell], _shell_SHSetLocalizedName, _shell_SHSetLocalizedName_cpp, shell.SHSetLocalizedName, shellapi/SHSetLocalizedName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll; Shell32.dll (version 5.6 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHSetLocalizedName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



