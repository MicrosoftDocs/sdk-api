---
UID: NF:syncmgr.ISyncMgrHandlerCollection.BindToHandler
title: ISyncMgrHandlerCollection::BindToHandler
author: windows-sdk-content
description: Instantiates a specified sync handler when called by Sync Center.
old-location: shell\ISyncMgrHandlerCollection_BindToHandler.htm
old-project: shell
ms.assetid: a3ae2427-7c7d-45b6-82ea-a8f5607f9623
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],ISyncMgrHandlerCollection interface, ISyncMgrHandlerCollection interface [Windows Shell],BindToHandler method, ISyncMgrHandlerCollection.BindToHandler, ISyncMgrHandlerCollection::BindToHandler, _shell_ISyncMgrHandlerCollection_BindToHandler, shell.ISyncMgrHandlerCollection_BindToHandler, syncmgr/ISyncMgrHandlerCollection::BindToHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandlerCollection.BindToHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

