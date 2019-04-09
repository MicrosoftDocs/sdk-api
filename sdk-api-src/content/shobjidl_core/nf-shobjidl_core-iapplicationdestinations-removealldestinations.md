---
UID: NF:shobjidl_core.IApplicationDestinations.RemoveAllDestinations
title: IApplicationDestinations::RemoveAllDestinations (shobjidl_core.h)
author: windows-sdk-content
description: Clears all destination entries from the Recent and Frequent categories in an application's Jump List.
old-location: shell\IApplicationDestinations_RemoveAllDestinations.htm
tech.root: shell
ms.assetid: bda83a9a-9759-47cc-8d15-ac55583a5810
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IApplicationDestinations interface [Windows Shell],RemoveAllDestinations method, IApplicationDestinations.RemoveAllDestinations, IApplicationDestinations::RemoveAllDestinations, RemoveAllDestinations, RemoveAllDestinations method [Windows Shell], RemoveAllDestinations method [Windows Shell],IApplicationDestinations interface, _shell_IApplicationDestinations_RemoveAllDestinations, shell.IApplicationDestinations_RemoveAllDestinations, shobjidl_core/IApplicationDestinations::RemoveAllDestinations
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IApplicationDestinations.RemoveAllDestinations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDestinations::RemoveAllDestinations


## -description


Clears all destination entries from the <b>Recent</b> and <b>Frequent</b> categories in an application's Jump List.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not remove items that the user has pinned to the Jump List. Those items cannot be removed programmatically; only the user can remove them. However, it does remove usage data for those pinned items. It also cannot remove items from custom categories or the task list.

If the application has an explicit Application User Model ID (AppUserModelID), you must call <a href="https://msdn.microsoft.com/d1cb0646-f028-48e4-b40d-f90a08152513">IApplicationDestinations::SetAppID</a> before you call this method.




## -see-also




<a href="https://msdn.microsoft.com/d425eb2c-75c7-431e-9607-11ea2e092178">IApplicationDestinations</a>



<a href="https://msdn.microsoft.com/d1c33908-8450-4baf-8598-535a1941820c">IApplicationDestinations::RemoveDestination</a>



<a href="https://msdn.microsoft.com/d1cb0646-f028-48e4-b40d-f90a08152513">IApplicationDestinations::SetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

