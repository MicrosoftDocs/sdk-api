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

# IApplicationDestinations::SetAppID


## -description


Specifies a unique Application User Model ID (AppUserModelID) for the application from whose taskbar button's Jump List the methods of this interface will remove destinations. This method is optional.


## -parameters




### -param pszAppID [in]

Type: <b>LPCWSTR</b>

Pointer to the AppUserModelID of the process whose taskbar button representation receives the Jump List.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the application has an explicit AppUserModelID, this method must be called before you call <a href="https://msdn.microsoft.com/bda83a9a-9759-47cc-8d15-ac55583a5810">RemoveAllDestinations</a> or <a href="https://msdn.microsoft.com/d1c33908-8450-4baf-8598-535a1941820c">RemoveDestination</a>.

After an AppUserModelID is specified through an object's <b>SetAppID</b> method, the AppUserModelID is saved in the object for that object's lifetime, providing that it is not overwritten by another call to <b>SetAppID</b>.

Some applications will not declare an explicit AppUserModelID and should not call this method. In that case, the application's identity is deduced when <a href="https://msdn.microsoft.com/d1c33908-8450-4baf-8598-535a1941820c">IApplicationDestinations::RemoveDestination</a> or <a href="https://msdn.microsoft.com/bda83a9a-9759-47cc-8d15-ac55583a5810">IApplicationDestinations::RemoveAllDestinations</a> are called. However, there is a performance benefit in avoiding those calculations, so applications that provide custom Jump Lists are encouraged to use <a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">explicit AppUserModelIDs</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/d425eb2c-75c7-431e-9607-11ea2e092178">IApplicationDestinations</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

