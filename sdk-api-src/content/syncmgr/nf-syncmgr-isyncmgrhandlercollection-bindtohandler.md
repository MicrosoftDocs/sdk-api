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

# ISyncMgrHandlerCollection::BindToHandler


## -description


Instantiates a specified sync handler when called by Sync Center.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

The ID of the sync handler.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the requested interface. This will typically be IID_ISyncMgrHandler. If the method fails when passed IID_ISyncMgrHandler, it is recalled using IID_ISyncMgrSynchronize, the IID of the older <a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a> interface. When the method returns successfully, a pointer to the requested interface is referenced in the <i>ppv</i> parameter.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains an address of a pointer to an interface representing the sync handler.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is possible for this method to be called by Sync Center without it first calling <a href="https://msdn.microsoft.com/9324b621-b29f-47b1-a691-603cb96497e7">ISyncMgrHandlerCollection::GetHandlerEnumerator</a>. This is because Sync Center caches information about handlers and their items. The handler collection can return an interface pointer for an existing sync handler or it can create a new instance.




## -see-also




<a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a>



<a href="https://msdn.microsoft.com/24514602-42c0-41ef-be33-fce03e7f091a">ISyncMgrHandlerCollection</a>
 

 

