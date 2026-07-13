---
UID: NF:shlwapi.GetMenuPosFromID
title: GetMenuPosFromID function (shlwapi.h)
description: GetMenuPosFromID may be altered or unavailable.
helpviewer_keywords: ["GetMenuPosFromID","GetMenuPosFromID function [Windows Shell]","_shell_GetMenuPosFromID","shell.GetMenuPosFromID","shlwapi/GetMenuPosFromID"]
old-location: shell\GetMenuPosFromID.htm
tech.root: shell
ms.assetid: 25fb51bc-9b36-4afb-bb07-7bc455c7fbc4
ms.date: 12/05/2018
ms.keywords: GetMenuPosFromID, GetMenuPosFromID function [Windows Shell], _shell_GetMenuPosFromID, shell.GetMenuPosFromID, shlwapi/GetMenuPosFromID
req.header: shlwapi.h
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.82 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMenuPosFromID
 - shlwapi/GetMenuPosFromID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - GetMenuPosFromID
---

# GetMenuPosFromID function


## -description

<p class="CCE_Message">[<b>GetMenuPosFromID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines the position of an item in a menu. Used in the case where the item's ID is known.

## -parameters

### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the menu.

### -param id

Type: <b>UINT</b>

An application-defined 16-bit value that identifies the menu item.

## -returns

Type: <b>int</b>

The item's zero-based position in the menu.

## -remarks

Beginning with Windows Vista, this function is declared in Shlwapi.h.

<b>Windows XP:  </b>This function is declared in Shlwapi.dll.

