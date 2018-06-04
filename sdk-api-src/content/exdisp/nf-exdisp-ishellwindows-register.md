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

# IShellWindows::Register


## -description


Registers an open window as a Shell window; the window is specified by handle.


## -parameters




### -param pid [in]

Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>*</b>

The window's <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface.


### -param hwnd [in]

Type: <b>long</b>

A handle that specifies the window to register.


### -param swClass [in]

Type: <b>int</b>

A member of <a href="https://msdn.microsoft.com/79d4fcf3-5256-4e21-ab9a-94605e1d742f">ShellWindowTypeConstants</a> that specifies the type of window.


### -param plCookie [out]

Type: <b>long*</b>

The window's cookie.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the context of the Shell windows collection, a <i>cookie</i> is a token that uniquely identifies a registered Shell window.

Use this method to register an open window; if the window is pending open, use <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a> instead.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>



<a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">IShellWindows::Revoke</a>
 

 

