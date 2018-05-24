---
UID: NF:exdisp.IShellWindows.OnNavigate
title: IShellWindows::OnNavigate
author: windows-driver-content
description: Occurs when a Shell window is navigated to a new location.
old-location: shell\IShellWindows_OnNavigate.htm
old-project: shell
ms.assetid: b65bc979-db32-48b3-b71f-fd389957b265
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IShellWindows interface [Windows Shell],OnNavigate method, IShellWindows.OnNavigate, IShellWindows::OnNavigate, OnNavigate, OnNavigate method [Windows Shell], OnNavigate method [Windows Shell],IShellWindows interface, _win32_IShellWindows_OnNavigate, exdisp/IShellWindows::OnNavigate, shell.IShellWindows_OnNavigate
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
-	IShellWindows.OnNavigate
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
req.product: Internet Explorer 5
---

# IShellWindows::OnNavigate


## -description


Occurs when a Shell window is navigated to a new location.


## -parameters




### -param lCookie [in]

Type: <b>long</b>

The cookie that identifies the window.


### -param pvarLoc [in]

Type: <b>VARIANT*</b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarLoc</i> to an absolute <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the new location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A window is granted a cookie when it is registered as a Shell window. For more information, see <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a>.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/ccd93f0f-3cd2-4b18-b6d2-834665d8b658">IShellWindows::OnActivated</a>



<a href="https://msdn.microsoft.com/ef2f75fe-dc93-403d-af1a-c08c45e2d818">IShellWindows::OnCreated</a>
 

 

