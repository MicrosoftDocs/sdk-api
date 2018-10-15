---
UID: NN:shobjidl_core.IExecuteCommandApplicationHostEnvironment
title: IExecuteCommandApplicationHostEnvironment
author: windows-sdk-content
description: Provides a single method that enables an application to determine whether its host is in desktop or immersive mode.
old-location: shell\IExecuteCommandApplicationHostEnvironment.htm
tech.root: shell
ms.assetid: c890d306-66df-4c29-88db-d54362ac018a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IExecuteCommandApplicationHostEnvironment, IExecuteCommandApplicationHostEnvironment interface [Windows Shell], IExecuteCommandApplicationHostEnvironment interface [Windows Shell],described, shell.IExecuteCommandApplicationHostEnvironment, shobjidl_core/IExecuteCommandApplicationHostEnvironment
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
 - IExecuteCommandApplicationHostEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecuteCommandApplicationHostEnvironment interface


## -description


Provides a single method that enables an application to determine whether its host is in desktop or immersive mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExecuteCommandApplicationHostEnvironment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExecuteCommandApplicationHostEnvironment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExecuteCommandApplicationHostEnvironment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba26f985-04f1-4a05-9363-a7be0585bcfc">GetValue</a>
</td>
<td align="left" width="63%">
Determines whether the current application host environment is in the desktop or immersive mode.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
An application must implement this interface together with the DelegateExecute handler (<a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a>).



