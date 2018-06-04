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

# ImmAssociateContext function


## -description


Associates the specified input context with the specified window. By default, the operating system associates the default input context with each window as it is created.
<div class="alert"><b>Note</b>  To specify a type of association, the application should use the <a href="https://msdn.microsoft.com/7f44d274-b5e9-4feb-acd6-5c68b3f7d868">ImmAssociateContextEx</a> function.</div><div> </div>

## -parameters




### -param HWND

TBD


### -param HIMC

TBD




#### - hIMC [in]

Handle to the input context. If <i>hIMC</i> is <b>NULL</b>, the function removes any association the window has with an input context. Thus IME cannot be used in the window.


#### - hWnd [in]

Handle to the window to associate with the input context.


## -returns



Returns the handle to the input context previously associated with the window.




## -remarks



When associating an input context with a window, an application must remove the association before destroying the input context. One way to do this is to save the handle and reassociate it to the default input context with the window.




## -see-also




<a href="https://msdn.microsoft.com/7f44d274-b5e9-4feb-acd6-5c68b3f7d868">ImmAssociateContextEx</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

