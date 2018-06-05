---
UID: NF:shobjidl_core.IExplorerBrowser.Unadvise
title: IExplorerBrowser::Unadvise
author: windows-sdk-content
description: Terminates an advisory connection.
old-location: shell\IExplorerBrowser_Unadvise.htm
old-project: shell
ms.assetid: a9b6b971-5676-4ceb-ab48-2350a1715b82
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],Unadvise method, IExplorerBrowser.Unadvise, IExplorerBrowser::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_Unadvise, shell.IExplorerBrowser_Unadvise, shobjidl_core/IExplorerBrowser::Unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IExplorerBrowser.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowser::Unadvise


## -description


Terminates an advisory connection.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A connection token previously returned from <a href="https://msdn.microsoft.com/b77f9c41-248e-4f16-a9ff-6ff5437df11c">IExplorerBrowser::Advise</a>. Identifies the connection to be terminated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Terminates an advisory connection previously established through method <a href="https://msdn.microsoft.com/b77f9c41-248e-4f16-a9ff-6ff5437df11c">IExplorerBrowser::Advise</a>. The <i>dwCookie</i> parameter identifies the connection to terminate. Failure to call  <b>IExplorerBrowser::Unadvise</b>, may result in a memory leak.



