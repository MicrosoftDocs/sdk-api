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
 

 

