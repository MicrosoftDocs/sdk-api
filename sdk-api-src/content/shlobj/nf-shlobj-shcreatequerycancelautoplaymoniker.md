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

# SHCreateQueryCancelAutoPlayMoniker function


## -description


<p class="CCE_Message">[This function is deprecated. Use <a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a> instead. Note that the CLSID used in the call to <b>CreateClassMoniker</b> must be application-defined. Do not call <b>CreateClassMoniker</b> with a system-defined CLSID.]

Deprecated. Creates a <b>QueryCancelAutoPlay</b> class moniker, which can then be used to register the <a href="https://msdn.microsoft.com/7dd470cd-163b-43e1-80d9-cdaa8b615858">IQueryCancelAutoPlay</a> handler in the running object table (ROT).


## -parameters




### -param ppmoniker [out]

Type: <b><a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>**</b>

The address of a <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface pointer that, when this function returns successfully, receives the <b>QueryCancelAutoPlay</b> class moniker. If this function call fails, this value is <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If successful, <b>SHCreateQueryCancelAutoPlayMoniker</b> calls the interface's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method and increments the reference count. When you are finished, call the interface's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to release.




## -see-also




<a href="https://msdn.microsoft.com/9361b2c1-ef26-4225-92ff-e0bef0285bc4">CreateClassMoniker</a>
 

 

