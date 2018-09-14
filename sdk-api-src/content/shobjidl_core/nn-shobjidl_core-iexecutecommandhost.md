---
UID: NN:shobjidl_core.IExecuteCommandHost
title: IExecuteCommandHost
author: windows-sdk-content
description: Provides a method that enables an IExplorerCommand-based Shell verb handler to query the UI mode of the host component from which the application was invoked.
old-location: shell\IExecuteCommandHost.htm
tech.root: shell
ms.assetid: ab75d502-c488-4511-9aa1-3af863b8e425
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IExecuteCommandHost, IExecuteCommandHost interface [Windows Shell], IExecuteCommandHost interface [Windows Shell],described, shell.IExecuteCommandHost, shobjidl_core/IExecuteCommandHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecuteCommandHost interface


## -description


Provides a method that enables an <a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a>-based Shell verb handler to query the UI mode of the host component from which the application was invoked.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExecuteCommandHost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExecuteCommandHost</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12132ffd-64a5-4104-8590-8eabfbc8268f">GetUIMode</a>
</td>
<td align="left" width="63%"></td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
A software component (either an OS component or an application) taat can launch a dual-mode application such as a browser should implement this interface. The interface should be implemented on an object that can be reached through the site chain provided to <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> or the context menu and retrieved through the <a href="https://msdn.microsoft.com/library/Cc678966(v=VS.85).aspx">IServiceProvider::QueryService</a> method.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
Typically, an application that is capable of launching as both a desktop application and a Windows Store app app will use this interface to query which mode the host is currently in. The application can then launch in the UI mode that is compatible with the host.



