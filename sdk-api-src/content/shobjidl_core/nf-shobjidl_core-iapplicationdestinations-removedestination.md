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
 

 

