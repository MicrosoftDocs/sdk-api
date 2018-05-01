---
UID: NF:exdisp.IShellWindows.OnActivated
title: IShellWindows::OnActivated method
author: windows-driver-content
description: Occurs when a Shell window's activation state changes.
old-location: shell\IShellWindows_OnActivated.htm
old-project: shell
ms.assetid: ccd93f0f-3cd2-4b18-b6d2-834665d8b658
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IShellWindows, IShellWindows interface [Windows Shell], OnActivated method, IShellWindows::OnActivated, OnActivated method [Windows Shell], OnActivated method [Windows Shell], IShellWindows interface, OnActivated,IShellWindows.OnActivated, _win32_IShellWindows_OnActivated, exdisp/IShellWindows::OnActivated, shell.IShellWindows_OnActivated
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdocvw.dll
api_name:
-	IShellWindows.OnActivated
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
req.product: Internet Explorer 5
---

# IShellWindows::OnActivated method


## -description


Occurs when a Shell window's activation state changes.


## -parameters




### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.


### -param fActive [in]

Type: <b>VARIANT_BOOL</b>

<b>TRUE</b> if the window is being activated; <b>FALSE</b> if the window is being deactivated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a>.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/ef2f75fe-dc93-403d-af1a-c08c45e2d818">IShellWindows::OnCreated</a>



<a href="https://msdn.microsoft.com/b65bc979-db32-48b3-b71f-fd389957b265">IShellWindows::OnNavigate</a>
 

 

