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

# IShellMenu::GetMenu


## -description


Gets the menu information set by calling <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>.


## -parameters




### -param phmenu [out]

Type: <b>HMENU*</b>

When this method returns, contains a pointer to an <b>HMENU</b> value that receives the <i>hmenu</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


### -param phwnd [out]

Type: <b>HWND*</b>

When this method returns, contains a pointer to an <b>HWND</b> value that receives the <i>hwnd</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to a <b>DWORD</b> value that receives the <i>dwFlags</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



