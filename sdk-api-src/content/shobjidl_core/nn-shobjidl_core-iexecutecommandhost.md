---
UID: NN:shobjidl_core.IExecuteCommandHost
title: IExecuteCommandHost (shobjidl_core.h)

description: Provides a method that enables an IExplorerCommand-based Shell verb handler to query the UI mode of the host component from which the application was invoked.
old-location: shell\IExecuteCommandHost.htm
tech.root: shell
ms.assetid: ab75d502-c488-4511-9aa1-3af863b8e425

ms.date: 12/05/2018
ms.keywords: IExecuteCommandHost, IExecuteCommandHost interface [Windows Shell], IExecuteCommandHost interface [Windows Shell],described, shell.IExecuteCommandHost, shobjidl_core/IExecuteCommandHost
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IExecuteCommandHost"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExecuteCommandHost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExecuteCommandHost interface


## -description


Provides a method that enables an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a>-based Shell verb handler to query the UI mode of the host component from which the application was invoked.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExecuteCommandHost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExecuteCommandHost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExecuteCommandHost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommandhost-getuimode">GetUIMode</a>
</td>
<td align="left" width="63%"></td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
A software component (either an OS component or an application) taat can launch a dual-mode application such as a browser should implement this interface. The interface should be implemented on an object that can be reached through the site chain provided to <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> or the context menu and retrieved through the <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a> method.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Typically, an application that is capable of launching as both a desktop application and a Windows Store app app will use this interface to query which mode the host is currently in. The application can then launch in the UI mode that is compatible with the host.



