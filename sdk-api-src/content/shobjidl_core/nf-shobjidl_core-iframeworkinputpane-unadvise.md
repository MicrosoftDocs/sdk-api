---
UID: NF:shobjidl_core.IFrameworkInputPane.Unadvise
title: IFrameworkInputPane::Unadvise (shobjidl_core.h)
author: windows-sdk-content
description: Unregisters an app's input pane handler object so that it no longer receives notifications.
old-location: shell\IFrameworkInputPane_Unadvise.htm
tech.root: shell
ms.assetid: E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFrameworkInputPane interface [Windows Shell],Unadvise method, IFrameworkInputPane.Unadvise, IFrameworkInputPane::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IFrameworkInputPane interface, shell.IFrameworkInputPane_Unadvise, shobjidl_core/IFrameworkInputPane::Unadvise
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFrameworkInputPane.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFrameworkInputPane::Unadvise


## -description


Unregisters an app's input pane handler object so that it no longer receives notifications.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A cookie that identifies the handler. This value was obtained when you registered the handler through the <a href="https://msdn.microsoft.com/F05A097F-13A4-48ad-B660-5B2409BB6D61">Advise</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/05C115BA-249A-4271-9C6F-DAAEE91BB936">IFrameworkInputPane</a>
 

 

