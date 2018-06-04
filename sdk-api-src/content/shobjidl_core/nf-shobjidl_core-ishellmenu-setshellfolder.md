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

# IShellMenu::SetShellFolder


## -description


Specifies the folder for the menu band to browse.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the folder's <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface. This pointer can be <b>NULL</b>.


### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The folder's fully qualified <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>. This value can be <b>NULL</b>.


### -param hKey [in]

Type: <b>HKEY</b>

An HKEY with an "Order" value that is used to store the order of the menu. This value can be <b>NULL</b>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify how the menu band operates.



#### SMSET_BOTTOM

Put this folder at the bottom of the menu.



#### SMSET_USEBKICONEXTRACTION

Use the background icon extractor.



#### SMSET_HASEXPANDABLEFOLDERS

This folder contains expandable folders.



#### SMSET_COLLAPSEONEMPTY

Collapse the menu if empty.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after you call <a href="https://msdn.microsoft.com/dc9864df-21f3-4b0b-b862-48055032c071">IShellMenu::Initialize</a>.



