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

# IShellFolder2::GetDefaultColumnState


## -description


Gets the default state for a specified column.


## -parameters




### -param iColumn [in]

Type: <b>UINT</b>

An integer that specifies the column number.


### -param pcsFlags [out]

Type: <b>SHCOLSTATEF*</b>

A pointer to a value that contains flags that indicate the default column state. This parameter can include a combination of the following flags.



#### SHCOLSTATE_TYPE_STR

A string.



#### SHCOLSTATE_TYPE_INT

An integer.



#### SHCOLSTATE_TYPE_DATE

A date.



#### SHCOLSTATE_ONBYDEFAULT

Should be shown by default in the Windows Explorer Details view.



#### SHCOLSTATE_SLOW

Recommends that the folder view extract column information asynchronously, on a background thread, because extracting this information can be time consuming.



#### SHCOLSTATE_EXTENDED

Provided by a handler, not the folder object.



#### SHCOLSTATE_SECONDARYUI

Not displayed in the shortcut menu, but listed in the More dialog box.



#### SHCOLSTATE_HIDDEN

Not displayed in the user interface.



#### SHCOLSTATE_PREFER_VARCMP

Uses default sorting rather than <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">CompareIDs</a> to get the sort order.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



