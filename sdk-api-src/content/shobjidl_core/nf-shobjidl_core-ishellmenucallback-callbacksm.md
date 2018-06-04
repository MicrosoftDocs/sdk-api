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

# IShellMenuCallback::CallbackSM


## -description


Receives messages from a menu band object.


## -parameters




### -param psmd [in, out]

Type: <b>LPSMDATA</b>

A pointer to a <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure that contains information about the menu.


### -param uMsg

Type: <b>UINT</b>

A message ID. This will be one of the SMC_XXX values. See <a href="https://msdn.microsoft.com/ea8329b4-a14e-4df0-9c15-ae0aea08744d">Shell Messages and Notifications</a> for a complete list.


### -param wParam

Type: <b>WPARAM</b>

A WPARAM value that contains additional information. See the specific SMC_XXX message reference for details.


### -param lParam

Type: <b>LPARAM</b>

An LPARAM value that contains additional information. See the specific SMC_XXX message reference for details.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



