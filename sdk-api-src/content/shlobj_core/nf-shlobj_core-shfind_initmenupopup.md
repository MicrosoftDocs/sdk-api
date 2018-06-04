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

# SHFind_InitMenuPopup function


## -description


<p class="CCE_Message">[<b>SHFind_InitMenuPopup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> instance for the submenu of options displayed for the <b>Search</b> entry in the Classic style Start menu.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the popup menu.


### -param hwndOwner

TBD


### -param idCmdFirst

Type: <b>UINT</b>

The ID of the first menu item.


### -param idCmdLast

Type: <b>UINT</b>

The ID of the last menu item.


#### - hwnd [in, optional]

Type: <b>HWND</b>

The handle of the popup menu's owner window. This value can be <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>*</b>

If successful, returns an <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> pointer. On failure, returns <b>NULL</b>.



