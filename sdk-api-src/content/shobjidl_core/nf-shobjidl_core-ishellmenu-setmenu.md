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

# IShellMenu::SetMenu


## -description


Appends a static menu to the menu band.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the static menu that is to be appended. This value can be <b>NULL</b>.


### -param hwnd [in]

Type: <b>HWND</b>

The <b>HWND</b> of the owner window. This value can be <b>NULL</b>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify how the menu operates.



#### SMSET_BOTTOM

Attach the menu to the bottom of the parent menu.



#### SMSET_TOP

Attach the menu to the top of the parent menu.



#### SMSET_DONTOWN

The menu band does not own the menu named in <i>hwnd</i>, so should that menu eventually be replaced, it should not be destroyed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



