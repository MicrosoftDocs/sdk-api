---
UID: NN:shobjidl_core.IExecuteCommandHost
title: IExecuteCommandHost (shobjidl_core.h)
description: Provides a method that enables an IExplorerCommand-based Shell verb handler to query the UI mode of the host component from which the application was invoked.
helpviewer_keywords: ["IExecuteCommandHost","IExecuteCommandHost interface [Windows Shell]","IExecuteCommandHost interface [Windows Shell]","described","shell.IExecuteCommandHost","shobjidl_core/IExecuteCommandHost"]
old-location: shell\IExecuteCommandHost.htm
tech.root: shell
ms.assetid: ab75d502-c488-4511-9aa1-3af863b8e425
ms.date: 12/05/2018
ms.keywords: IExecuteCommandHost, IExecuteCommandHost interface [Windows Shell], IExecuteCommandHost interface [Windows Shell],described, shell.IExecuteCommandHost, shobjidl_core/IExecuteCommandHost
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExecuteCommandHost
 - shobjidl_core/IExecuteCommandHost
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExecuteCommandHost
---

# IExecuteCommandHost interface


## -description

Provides a method that enables an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a>-based Shell verb handler to query the UI mode of the host component from which the application was invoked.

## -inheritance

The <b>IExecuteCommandHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExecuteCommandHost</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
A software component (either an OS component or an application) taat can launch a dual-mode application such as a browser should implement this interface. The interface should be implemented on an object that can be reached through the site chain provided to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> or the context menu and retrieved through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a> method.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Typically, an application that is capable of launching as both a desktop application and a Windows Store app will use this interface to query which mode the host is currently in. The application can then launch in the UI mode that is compatible with the host.
