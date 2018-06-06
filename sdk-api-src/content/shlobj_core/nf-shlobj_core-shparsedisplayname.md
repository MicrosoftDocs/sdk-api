---
UID: NF:shlobj_core.SHParseDisplayName
title: SHParseDisplayName function
author: windows-sdk-content
description: Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object. This function is the preferred method to convert a string to a pointer to an item identifier list (PIDL).
old-location: shell\SHParseDisplayName.htm
old-project: shell
ms.assetid: 7bdfeed5-dcd0-40f6-a9d0-08ce816ee055
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHParseDisplayName, SHParseDisplayName function [Windows Shell], _shell_SHParseDisplayName, shell.SHParseDisplayName, shlobj_core/SHParseDisplayName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHParseDisplayName
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHParseDisplayName function


## -description


Translates a Shell namespace object's display name into an item identifier list and returns the attributes of the object. This function is the preferred method to convert a string to a pointer to an item identifier list (PIDL).


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a zero-terminated wide string that contains the display name to parse.


### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A bind context that controls the parsing operation. This parameter is normally set to <b>NULL</b>.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The address of a pointer to a variable of type <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> that receives the item identifier list for the object. If an error occurs, then this parameter is set to <b>NULL</b>.


### -param sfgaoIn [in]

Type: <b>SFGAOF</b>

A <b>ULONG</b> value that specifies the attributes to query. To query for one or more attributes, initialize this parameter with the flags that represent the attributes of interest. For a list of available SFGAO flags, see <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


### -param psfgaoOut [out, optional]

Type: <b>SFGAOF*</b>

A pointer to a <b>ULONG</b>. On return, those attributes that are true for the object and were requested in <i>sfgaoIn</i> are set. An object's attribute flags can be zero or a combination of SFGAO flags. For a list of available SFGAO flags, see <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You should call this function from a background thread. Failure to do so could cause the UI to stop responding.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>



<a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a>



<a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>



<a href="https://msdn.microsoft.com/f043ffa2-37c1-465d-aed6-0475e721fbde">SHGetPathFromIDList</a>
 

 

