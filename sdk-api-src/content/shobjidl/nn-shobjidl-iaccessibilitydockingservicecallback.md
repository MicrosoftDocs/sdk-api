---
UID: NN:shobjidl.IAccessibilityDockingServiceCallback
title: IAccessibilityDockingServiceCallback
author: windows-sdk-content
description: Informs an accessibility app that its window has been undocked.
old-location: shell\IAccessibilityDockingServiceCallback.htm
tech.root: shell
ms.assetid: E357E47C-5A29-4b92-AD26-E604E501B7D6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAccessibilityDockingServiceCallback, IAccessibilityDockingServiceCallback interface [Windows Shell], IAccessibilityDockingServiceCallback interface [Windows Shell],described, shell.IAccessibilityDockingServiceCallback, shobjidl/IAccessibilityDockingServiceCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
 - Shobjidl.h
api_name:
 - IAccessibilityDockingServiceCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibilityDockingServiceCallback interface


## -description


Informs an accessibility app that its window has been undocked.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibilityDockingServiceCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibilityDockingServiceCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibilityDockingServiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AFD60F5B-3017-49a2-8AFC-8309D11B3ACA">Undocked</a>
</td>
<td align="left" width="63%">
Called when the accessibility window has been undocked, giving the app the chance to redock.

</td>
</tr>
</table> 


## -remarks



Pass a pointer to the object that implements this interface when you call <a href="https://msdn.microsoft.com/D7B2AC62-D044-45b6-AF12-9BAC32A3B114">IAccessibilityDockingService::DockWindow</a>.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
You must implement this interface in order to use the accessibility app docking feature and be notified of undock events.



