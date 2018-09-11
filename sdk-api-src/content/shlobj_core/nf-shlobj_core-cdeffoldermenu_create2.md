---
UID: NF:shlobj_core.CDefFolderMenu_Create2
title: CDefFolderMenu_Create2 function
author: windows-sdk-content
description: Creates a context menu for a selected group of file folder objects.
old-location: shell\CDefFolderMenu_Create2.htm
tech.root: shell
ms.assetid: 7b5e012d-1c8b-42c5-8181-9923fd389fc5
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CDefFolderMenu_Create2, CDefFolderMenu_Create2 function [Windows Shell], _win32_CDefFolderMenu_Create2, shell.CDefFolderMenu_Create2, shlobj_core/CDefFolderMenu_Create2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - CDefFolderMenu_Create2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CDefFolderMenu_Create2 function


## -description


Creates a context menu for a selected group of file folder objects.


## -parameters




### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

An <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure for the parent folder. This value can be <b>NULL</b>.


### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window. This value can be <b>NULL</b>.


### -param cidl

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures in the array pointed to by <i>apidl</i>.


### -param apidl [in, optional]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures, one for each item that is selected.


### -param psf [in, optional]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the parent folder's <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface. This <b>IShellFolder</b> must support the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface. If it does not, <b>CDefFolderMenu_Create2</b> fails and returns E_NOINTERFACE. This value can be <b>NULL</b>.


### -param pfn [in, optional]

Type: <b><a href="https://msdn.microsoft.com/a5635196-80de-4db9-9c3a-65f2b241b4a0">LPFNDFMCALLBACK</a></b>

The <a href="https://msdn.microsoft.com/a5635196-80de-4db9-9c3a-65f2b241b4a0">LPFNDFMCALLBACK</a> callback object. This value can be <b>NULL</b> if the callback object is not needed.


### -param nKeys

Type: <b>UINT</b>

The number of registry keys in the array pointed to by <i>ahkeys</i>.



<div class="alert"><b>Note</b>  The maximum number of registry keys is 16. Callers must enforce this limit as the API does not. Failing to do so can result in memory corruption.</div>
<div> </div>

### -param ahkeys [in, optional]

Type: <b>const HKEY*</b>

A pointer to an array of registry keys that specify the context menu handlers used with the menu's entries. For more information on context menu handlers, see <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">Creating Context Menu Handlers</a>. This array can contain a maximum of 16 registry keys.


### -param ppcm [out]

Type: <b><a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>**</b>

The address of an <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface pointer that, when this function returns successfully, points to the <b>IContextMenu</b> object that represents the context menu.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/055ff0a0-9ba7-463d-9684-3fd072b190da">SHCreateDefaultContextMenu</a>
 

 

