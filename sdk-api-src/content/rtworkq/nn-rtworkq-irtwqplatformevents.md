---
UID: NN:rtworkq.IRtwqPlatformEvents
title: IRtwqPlatformEvents
author: windows-sdk-content
description: Provides events related platform work queue.
old-location: base\irtwqplatformevents.htm
tech.root: procthread
ms.assetid: 9184D930-9305-4CA0-8E89-0CBAA5E4D53F
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IRtwqPlatformEvents, IRtwqPlatformEvents interface, IRtwqPlatformEvents interface,described, base.irtwqplatformevents, rtworkq/IRtwqPlatformEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqPlatformEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRtwqPlatformEvents interface


## -description


Provides events related platform work queue.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRtwqPlatformEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRtwqPlatformEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRtwqPlatformEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7CAD2809-9030-4D84-9FF4-A2461EB18583">InitializationComplete</a>
</td>
<td align="left" width="63%">
Called after the platform has been initialized.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03F4F1D8-8A90-4DDE-B0BC-8F10EBA9691E">ShutdownComplete</a>
</td>
<td align="left" width="63%">
Called after the platform has  shutdown. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B2D3F35E-B859-4735-A11C-B3CB6ACD81EC">ShutdownStart</a>
</td>
<td align="left" width="63%">
Called before the platform is about to shutdown. 

</td>
</tr>
</table> 

