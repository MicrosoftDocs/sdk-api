---
UID: NF:syncmgr.ISyncMgrEvent.GetContext
title: ISyncMgrEvent::GetContext
author: windows-sdk-content
description: Gets a context object that can be used by a handler to display properties or execute a context menu action.
old-location: shell\ISyncMgrEvent_GetContext.htm
old-project: shell
ms.assetid: 849e2bfe-daf7-422a-909c-03608ef1e325
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetContext, GetContext method [Windows Shell], GetContext method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetContext method, ISyncMgrEvent.GetContext, ISyncMgrEvent::GetContext, _shell_ISyncMgrEvent_GetContext, shell.ISyncMgrEvent_GetContext, syncmgr/ISyncMgrEvent::GetContext
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
 - ISyncMgrEvent.GetContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetContext


## -description


Gets a context object that can be used by a handler to display properties or execute a context menu action.


## -parameters




### -param ppszContext [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to the context as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The handler is expected to allocate the buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



