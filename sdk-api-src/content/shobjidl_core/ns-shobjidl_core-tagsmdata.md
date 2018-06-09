---
UID: NS:shobjidl_core.tagSMDATA
title: tagSMDATA
author: windows-sdk-content
description: Contains information from a menu band.
old-location: shell\SMDATA.htm
old-project: shell
ms.assetid: 4690daa1-f935-4d0c-8b1f-0b9442fc78dc
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*LPSMDATA, SMDATA, SMDATA structure [Windows Shell], _win32_SMDATA, lPSMDATA, lPSMDATA structure pointer [Windows Shell], shell.SMDATA, shobjidl_core/SMDATA, shobjidl_core/lPSMDATA, tagSMDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SMDATA, *LPSMDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SMDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# tagSMDATA structure


## -description


Contains information from a menu band.


## -struct-fields




### -field dwMask

Type: <b>DWORD</b>

A mask that is always set to SMDM_HMENU.


### -field dwFlags

Type: <b>DWORD</b>


### -field hmenu

Type: <b>HMENU</b>

The static menu portion of the menu band.


### -field hwnd

Type: <b>HWND</b>

The HWND value of the owner window.


### -field uId

Type: <b>UINT</b>

The identifier of the menu item. This value is -1 for the menu itself.


### -field uIdParent

Type: <b>UINT</b>

The identifier of the parent menu.


### -field uIdAncestor

Type: <b>UINT</b>


### -field punk

Type: <b>IUknown*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the <a href="https://msdn.microsoft.com/3b9e65d4-a881-4e13-9487-87de9d560377">MenuBand</a> object.


### -field pidlFolder

Type: <b>PIDLIST_ABSOLUTE</b>

The <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> of the shell folder portion of the menu.


### -field pidlItem

Type: <b>PUITEMID_CHILD</b>

The <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> of the selected item in the shell folder portion of the menu.


### -field psf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface for the folder associated with the shell folder portion of the menu.


### -field pvUserData

Type: <b>void*</b>

A pointer to a user-defined data structure.

