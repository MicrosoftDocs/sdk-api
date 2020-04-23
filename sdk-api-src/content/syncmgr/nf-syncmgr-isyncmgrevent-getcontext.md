---
UID: NF:syncmgr.ISyncMgrEvent.GetContext
title: ISyncMgrEvent::GetContext (syncmgr.h)
description: Gets a context object that can be used by a handler to display properties or execute a context menu action.helpviewer_keywords: ["GetContext","GetContext method [Windows Shell]","GetContext method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetContext method","ISyncMgrEvent.GetContext","ISyncMgrEvent::GetContext","_shell_ISyncMgrEvent_GetContext","shell.ISyncMgrEvent_GetContext","syncmgr/ISyncMgrEvent::GetContext"]
old-location: shell\ISyncMgrEvent_GetContext.htm
tech.root: shell
ms.assetid: 849e2bfe-daf7-422a-909c-03608ef1e325
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Windows Shell], GetContext method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetContext method, ISyncMgrEvent.GetContext, ISyncMgrEvent::GetContext, _shell_ISyncMgrEvent_GetContext, shell.ISyncMgrEvent_GetContext, syncmgr/ISyncMgrEvent::GetContext
f1_keywords:
- syncmgr/ISyncMgrEvent.GetContext
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Syncmgr.h
api_name:
- ISyncMgrEvent.GetContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The handler is expected to allocate the buffer using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



