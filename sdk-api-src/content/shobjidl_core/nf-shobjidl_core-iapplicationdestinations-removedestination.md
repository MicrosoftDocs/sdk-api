---
UID: NF:shobjidl_core.IApplicationDestinations.RemoveDestination
title: IApplicationDestinations::RemoveDestination
author: windows-sdk-content
description: Removes a single destination from the Recent and Frequent categories in a Jump List.
old-location: shell\IApplicationDestinations_RemoveDestination.htm
tech.root: shell
ms.assetid: d1c33908-8450-4baf-8598-535a1941820c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IApplicationDestinations interface [Windows Shell],RemoveDestination method, IApplicationDestinations.RemoveDestination, IApplicationDestinations::RemoveDestination, RemoveDestination, RemoveDestination method [Windows Shell], RemoveDestination method [Windows Shell],IApplicationDestinations interface, _shell_IApplicationDestinations_RemoveDestination, shell.IApplicationDestinations_RemoveDestination, shobjidl_core/IApplicationDestinations::RemoveDestination
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IApplicationDestinations.RemoveDestination
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDestinations::RemoveDestination


## -description


Removes a single destination from the <b>Recent</b> and <b>Frequent</b> categories in a Jump List.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> that represents the destination to remove.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a standard COM error value otherwise. If the object pointed to by <i>punk</i> is not an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a>, the method returns E_INVALIDARG.




## -remarks



A destination can appear in both the <b>Recent</b> and <b>Frequent</b> categories. If that is the case, this method removes the destination from both categories.

If the item is pinned to the list by the user, it is not removed but its usage data is cleared.

An application can call <b>RemoveDestination</b> without knowing if the item pointed to by <i>punk</i> is currently in the list. If there is no existing data on the item (in which case it is not in the <b>Recent</b> or <b>Frequent</b> list), this method does nothing and returns S_OK.

If the application has an explicit Application User Model ID (AppUserModelID), you must call <a href="https://msdn.microsoft.com/d1cb0646-f028-48e4-b40d-f90a08152513">IApplicationDestinations::SetAppID</a> before you call this method.




## -see-also




<a href="https://msdn.microsoft.com/d425eb2c-75c7-431e-9607-11ea2e092178">IApplicationDestinations</a>



<a href="https://msdn.microsoft.com/bda83a9a-9759-47cc-8d15-ac55583a5810">IApplicationDestinations::RemoveAllDestinations</a>



<a href="https://msdn.microsoft.com/d1cb0646-f028-48e4-b40d-f90a08152513">IApplicationDestinations::SetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

