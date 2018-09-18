---
UID: NF:shdeprecated.IBrowserService2._TryShell2Rename
title: IBrowserService2::_TryShell2Rename
author: windows-sdk-content
description: Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.
old-location: shell\IBrowserService2__TryShell2Rename.htm
tech.root: shell
ms.assetid: 30801c5d-151b-4556-a1e5-1cbc81a5c33a
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_TryShell2Rename method, IBrowserService2._TryShell2Rename, IBrowserService2::_TryShell2Rename, _TryShell2Rename, _TryShell2Rename method [Windows Shell], _TryShell2Rename method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_TryShell2Rename, shell.IBrowserService2__TryShell2Rename, zone_IBrowserService2__TryShell2Rename
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - IBrowserService2._TryShell2Rename
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_TryShell2Rename


## -description


Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.


## -parameters




### -param psv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> representing the current browser view.


### -param pidlNew [in]

Type: <b>LPCITEMIDLIST</b>

A PIDL that indicates the new name of the browser view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called in response to <a href="https://msdn.microsoft.com/a37c20b9-e2c6-438b-9fd5-749c680d5ee0">NotifyRedirect</a>.



