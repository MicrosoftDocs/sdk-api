---
UID: NF:shobjidl_core.IExplorerBrowser.Destroy
title: IExplorerBrowser::Destroy
author: windows-sdk-content
description: Destroys the browser.
old-location: shell\IExplorerBrowser_Destroy.htm
old-project: shell
ms.assetid: b6fc4aa6-f689-4b3e-a922-f8361d33b6dd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Destroy, Destroy method [Windows Shell], Destroy method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],Destroy method, IExplorerBrowser.Destroy, IExplorerBrowser::Destroy, _shell_IExplorerBrowser_Destroy, shell.IExplorerBrowser_Destroy, shobjidl_core/IExplorerBrowser::Destroy
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.Destroy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowser::Destroy


## -description


Destroys the browser.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If method <a href="https://msdn.microsoft.com/4b86646a-a20c-4bb5-a4c8-5c2e11e18862">IExplorerBrowser::Initialize</a> was called., then method <b>IExplorerBrowser::Destroy</b> must be called to free resources. Failure to call <b>IExplorerBrowser::Destroy</b> may cause a memory leak.



