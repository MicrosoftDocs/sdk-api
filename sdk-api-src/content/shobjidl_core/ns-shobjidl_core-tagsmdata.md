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

