---
UID: NN:shobjidl_core.IPackageExecutionStateChangeNotification
title: IPackageExecutionStateChangeNotification
author: windows-sdk-content
description: Enables receiving package state-change notifications during Windows Store app debugging.
old-location: shell\IPackageExecutionStateChangeNotification.htm
old-project: shell
ms.assetid: 6AD9A9CD-933B-432F-A124-48092588C5DF
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IPackageExecutionStateChangeNotification, IPackageExecutionStateChangeNotification interface [Windows Shell], IPackageExecutionStateChangeNotification interface [Windows Shell],described, shell.IPackageExecutionStateChangeNotification, shobjidl_core/IPackageExecutionStateChangeNotification
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPackageExecutionStateChangeNotification
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IPackageExecutionStateChangeNotification interface


## -description


Enables receiving package state-change notifications during Windows Store app debugging.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPackageExecutionStateChangeNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPackageExecutionStateChangeNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPackageExecutionStateChangeNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/254986AF-4572-4D63-B055-1C05A8FB0417">OnStateChanged</a>
</td>
<td align="left" width="63%">
Called when package state changes during Windows Store app debugging.

</td>
</tr>
</table> 


## -remarks



Implement the <b>IPackageExecutionStateChangeNotification</b> interface when you need to receive package state-change notifications during Windows Store app debugging. 

Call the <a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a> method to register for package state-change notifications.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>
 

 

