---
UID: NF:exdisp.IShellWindows.OnCreated
title: IShellWindows::OnCreated
author: windows-sdk-content
description: Occurs when a new Shell window is created for a frame.
old-location: shell\IShellWindows_OnCreated.htm
tech.root: shell
ms.assetid: ef2f75fe-dc93-403d-af1a-c08c45e2d818
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IShellWindows interface [Windows Shell],OnCreated method, IShellWindows.OnCreated, IShellWindows::OnCreated, OnCreated, OnCreated method [Windows Shell], OnCreated method [Windows Shell],IShellWindows interface, _win32_IShellWindows_OnCreated, exdisp/IShellWindows::OnCreated, shell.IShellWindows_OnCreated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.OnCreated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IShellWindows::OnCreated


## -description


Occurs when a new Shell window is created for a frame.


## -parameters




### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.


### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The address of the new window's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a>.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/ccd93f0f-3cd2-4b18-b6d2-834665d8b658">IShellWindows::OnActivated</a>



<a href="https://msdn.microsoft.com/b65bc979-db32-48b3-b71f-fd389957b265">IShellWindows::OnNavigate</a>
 

 

