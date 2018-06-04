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

# IShellExtInit::Initialize


## -description


Initializes a property sheet extension, shortcut menu extension, or drag-and-drop handler.


## -parameters




### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that uniquely identifies a folder. For property sheet extensions, this parameter is <b>NULL</b>. For shortcut menu extensions, it is the item identifier list for the folder that contains the item whose shortcut menu is being displayed. For nondefault drag-and-drop menu extensions, this parameter specifies the target folder.


### -param pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface object that can be used to retrieve the objects being acted upon.


### -param hkeyProgID [in]

Type: <b>HKEY</b>

The registry key for the file object or folder type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The meanings of some parameters depend on the extension type. For drag-and-drop handlers, the <i>pidlFolder</i> parameter specifies the destination folder (the drop target), the <i>pdtobj</i> parameter identifies the items being dropped, and the <i>hkeyProgID</i> parameter specifies the file type of the destination folder.

For <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">shortcut menu extensions</a>, <i>pdtobj</i> identifies the selected file objects, <i>hkeyProgID</i> identifies the <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">file type</a> of the object with focus, and <i>pidlFolder</i> is either <b>NULL</b> (for file objects) or specifies the folder for which the shortcut menu is being requested (for folder background shortcut menus).

For property sheet extensions, <i>pidlFolder</i> is <b>NULL</b>, <i>pdtobj</i> identifies the selected file objects, and <i>hkeyProgID</i> specifies the file type of the file object that has the focus.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This is the first method that the Shell calls after it creates an instance of a property sheet extension, shortcut menu extension, or drag-and-drop handler.



